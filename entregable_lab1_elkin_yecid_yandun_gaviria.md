# Entregable Laboratorio 1: Benchmarking de Serving Local y Cuantización

- **Curso:** LLMOps, Serving Local y Arquitecturas RAG
- **Estudiante:** Elkin Yecid Yandun Gaviria
- **Hardware Utilizado:** CPU: 8 CPU, 5.2 GB RAM, Ubuntu 26.04.1 LTS; VM de Docker Desktop ampliada a 3 GB
- **Fecha:** 13 de noviembre de 2026

---

## Análisis Técnico de Resultados

### 1. Impacto en Memoria (MEM USAGE y KV Cache)
> ¿Cuál fue la diferencia exacta en MB/GB de RAM consumida entre `q4_K_M` y `q8_0` al ejecutar `docker stats`? ¿Por qué el consumo en ejecución supera el tamaño del archivo en disco?

**Respuesta:**
las estadisticas de docker stats mostró una mediana de 1263 MiB para q4_K_M (rango 1242-1287 MiB) y 1920 MiB para q8_0 (rango 1822-1921 MiB).
La diferencia es de aproximadamente 657 MiB (0.64 GiB), el consumo en ejecución supera el archivo en disco porque, además de los pesos (986 MB y 1.6 GB), Ollama reserva el KV Cache para num_ctx=2048 y buffers del runtime: el sobrecosto medido fue de unos 277 MiB en q4_K_M y 282 MiB en q8_0.

---

### 2. Ancho de Banda de Memoria y Velocidad (TPS)
> En inferencia sobre CPU, el cuello de botella suele ser el ancho de banda de la memoria RAM. ¿En qué porcentaje aumentó la velocidad (TPS) al pasar de 8 bits a 4 bits?

**Respuesta:**
El TPS fue 17.66 en q4_K_M y 10.92 en q8_0, un aumento del 6,74 al pasar de 8 a 4 bits. Por prompt: Corto 18.93 vs 12.45 TPS (+6,48), Medio 17.42 vs 11.76 (+5,66) y Largo 16.62 vs 8.55 (+8,07). 
La mejora se debe por el menor volumen de datos que deben leerse desde RAM en cada token, en CPU el ancho de banda de memoria es el cuello de botella, por lo que mover aproximadamente la mitad de bytes por peso acelera la generación.

---

### 3. Latencia Inicial (TTFT) y Fase Prefill
> ¿Por qué el `TTFT (ms)` es significativamente más alto en el Prompt Largo que en el Prompt Corto?

**Respuesta:**
El TTFT del prompt Largo fue 1258 ms en q4_K_M y 1641 ms en q8_0, frente a 685 ms y 1148 ms del prompt Corto. En la fase Prefill el modelo procesa todos los tokens de entrada antes de emitir el primero; al aumentar la longitud crece el número de operaciones de atención y, por tanto, la latencia inicial por lo tanto es más notorio en el prompt de código, que es el más extenso de los tres.

---

### 4. Calidad vs. Eficiencia en `resultados_benchmark.md`
> Revisando las 6 respuestas completas generadas, ¿hubo alguna degradación perceptible en la lógica del código Python o en el razonamiento generado por el modelo de 4 bits frente al de 8 bits?

**Respuesta:**
Sí tiene diferencias, aunque no una degradación clara del 4 bits frente al 8 bits:
En el prompt Corto ambos modelos confundieron cuantización con tokenización o codificación, por lo que la respuesta de ambos modelos es incorrecta. 
En el prompt Medio, q4_K_M fue repetitivo y propuso modelos comerciales (Claude/Anthropic) para un servidor local sin GPU, mientras que q8_0 mantuvo una estructura más coherente. 
En el código Python, ambos implementaron correctamente la búsqueda binaria, q4_K_M incluyó más aserciones pero varias fallan por el manejo de excepciones y q8_0 documentó los casos sin ejecutarlos. 
Tiene una leve ventaja de q8_0 en coherencia del razonamiento.

---
*Nota: Adjuntar junto con este documento los archivos generados `resultados_benchmark.csv` y `resultados_benchmark.md`.*
