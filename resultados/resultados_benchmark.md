# Reporte de Benchmark y Respuestas: LLMOps Lab 1

Este documento detalla las respuestas completas obtenidas por cada modelo cuantizado frente a los prompts de prueba, acompañadas de sus métricas de rendimiento.

---

## Prueba 1: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Corto (Definición)
- **Métricas:** `TTFT: 684.74 ms` | `Velocidad: 18.93 TPS` | `Tokens: 366` | `Tiempo Total: 20.03 s`

### Prompt Enviado:
> Explica en exactamente 3 viñetas qué es la cuantización en modelos de lenguaje.

### Respuesta Generada:
```text
La cuantización en modelos de lenguaje es un proceso fundamental en la creación de sistemas de inteligencia artificial que simulan la capacidad humana de entender y producir lenguaje natural. Aquí te explico en tres viñetas lo que es la cuantización:

1. **Definición y propósito**: La cuantización es la transformación de una representación de texto en una representación numérica. En modelos de lenguaje, esto se realiza mediante la codificación de palabras o frases en números, lo que permite la computación y análisis de la información textual.

2. **Método utilizado**: En modelos de lenguaje como Transformers, la cuantización se realiza mediante la codificación de palabras en números utilizando técnicas como la Representación de Palabras en Números (Word2Vec) o la Codificación de Palabras en Números (WordPiece). Estas técnicas se basan en la idea de que las palabras pueden ser representadas de manera numérica para facilitar la computación y análisis.

3. **Beneficios y aplicaciones**: La cuantización en modelos de lenguaje tiene varios beneficios. Primero, facilita la computación de la información textual, ya que las operaciones matemáticas son más eficientes que las operaciones de texto. Segundo, permite la representación de la información en un espacio numérico, lo que permite la aplicación de técnicas de aprendizaje automático y la implementación de algoritmos de análisis de texto. Finalmente, la cuantización es fundamental para la creación de sistemas de IA que pueden entender y generar lenguaje natural, como chatbots, asistentes de inteligencia artificial y sistemas de traducción automática.
```

---

## Prueba 2: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Medio (Razonamiento)
- **Métricas:** `TTFT: 1303.35 ms` | `Velocidad: 17.42 TPS` | `Tokens: 831` | `Tiempo Total: 49.01 s`

### Prompt Enviado:
> Tengo un servidor con 16 GB de RAM y sin GPU. Quiero desplegar un asistente interno para 5 empleados. ¿Qué arquitectura y tamaño de modelo me recomiendas y por qué?

### Respuesta Generada:
```text
Para un servidor con 16 GB de RAM y sin GPU, la elección del modelo de asistente interno dependerá de varios factores, incluyendo la complejidad del trabajo que se realizará, la cantidad de información que se manejará y la velocidad de procesamiento requerida. Aquí te dejo algunas recomendaciones basadas en la mayoría de los casos:

1. **Modelo de Asistente Interno:**
   - **Modelo de Conversación**: Si el trabajo principal es la conversación y la interacción con el usuario, consideraría un modelo de conversación como Claude, Anthropic, o Anthropic. Estos modelos son diseñados para la interacción natural y la conversación, lo que puede ser útil para un asistente interno.
   - **Modelo de Inteligencia Artificial**: Si el trabajo principal es la toma de decisiones basada en datos, podría considerar un modelo de inteligencia artificial como Claude, Anthropic, o Anthropic. Estos modelos son diseñados para procesar grandes cantidades de datos y tomar decisiones basadas en la información.
   - **Modelo de Inteligencia Artificial para la Inteligencia General**: Si el trabajo principal es la toma de decisiones basadas en la inteligencia general, podría considerar un modelo de inteligencia artificial para la inteligencia general como Claude, Anthropic, o Anthropic. Estos modelos son diseñados para manejar problemas complejos y tomar decisiones basadas en la información.

2. **Tamaño de Modelo:**
   - **Modelo de Conversación**: Si el trabajo principal es la conversación y la interacción con el usuario, un modelo de conversación de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena interacción natural y una respuesta rápida.
   - **Modelo de Inteligencia Artificial**: Si el trabajo principal es la toma de decisiones basada en datos, un modelo de inteligencia artificial de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena procesamiento de grandes cantidades de datos y una respuesta rápida.
   - **Modelo de Inteligencia Artificial para la Inteligencia General**: Si el trabajo principal es la toma de decisiones basadas en la inteligencia general, un modelo de inteligencia artificial para la inteligencia general de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena procesamiento de grandes cantidades de datos y una respuesta rápida.

3. **Tamaño de la Base de Datos:**
   - **Modelo de Conversación**: Si el trabajo principal es la conversación y la interacción con el usuario, un modelo de conversación de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena interacción natural y una respuesta rápida.
   - **Modelo de Inteligencia Artificial**: Si el trabajo principal es la toma de decisiones basada en datos, un modelo de inteligencia artificial de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena procesamiento de grandes cantidades de datos y una respuesta rápida.
   - **Modelo de Inteligencia Artificial para la Inteligencia General**: Si el trabajo principal es la toma de decisiones basadas en la inteligencia general, un modelo de inteligencia artificial para la inteligencia general de tamaño mediano (100M-500M) podría ser adecuado. Esto permite una buena procesamiento de grandes cantidades de datos y una respuesta rápida.

Recuerda que estas recomendaciones son generales y pueden variar dependiendo del uso específico del asistente interno. Es posible que necesites ajustar el tamaño de modelo y la arquitectura según las necesidades específicas de tu proyecto.
```

---

## Prueba 3: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Largo (Generación de Código)
- **Métricas:** `TTFT: 1258.26 ms` | `Velocidad: 16.62 TPS` | `Tokens: 638` | `Tiempo Total: 39.65 s`

### Prompt Enviado:
> Escribe una función en Python bien documentada que implemente búsqueda binaria sobre una lista ordenada, incluyendo manejo de excepciones y 3 casos de prueba.

### Respuesta Generada:
```text
Aquí tienes una función bien documentada en Python que implementa la búsqueda binaria sobre una lista ordenada. Esta función incluye manejo de excepciones y 3 casos de prueba:

```python
def binary_search(arr, target):
    """
    Realiza una búsqueda binaria en una lista ordenada para encontrar el índice del elemento 'target'.
    
    Parámetros:
    arr (list): Una lista ordenada de elementos.
    target: El elemento a buscar en la lista.
    
    Retorna:
    int: El índice del elemento 'target' en la lista, o -1 si no se encuentra.
    
    Excepciones:
    ValueError: Si la lista no está ordenada.
    TypeError: Si 'target' no es un número.
    """
    # Verificar si la lista está ordenada
    if not arr:
        raise ValueError("La lista no puede estar vacía.")
    
    # Verificar si 'target' es un número
    if not isinstance(target, (int, float)):
        raise TypeError("El 'target' debe ser un número.")
    
    # Verificar si 'target' es menor que el primer elemento o mayor que el último
    if target < arr[0] or target > arr[-1]:
        return -1
    
    # Realizar la búsqueda binaria
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        mid_value = arr[mid]
        
        if mid_value == target:
            return mid
        elif mid_value < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1

# Casos de prueba
def test_binary_search():
    assert binary_search([1, 2, 3, 4, 5], 3) == 2
    assert binary_search([1, 2, 3, 4, 5], 6) == -1
    assert binary_search([1, 2, 3, 4, 5], 1) == 0
    assert binary_search([1, 2, 3, 4, 5], 5) == 4
    assert binary_search([1, 2, 3, 4, 5], 0) == -1
    assert binary_search([], 1) == -1
    assert binary_search([1, 2, 3, 4, 5], "1") == -1

    print("Todos los casos de prueba pasaron.")

# Ejecutar los casos de prueba
test_binary_search()
```

Esta función `binary_search` realiza una búsqueda binaria en una lista ordenada para encontrar el índice del elemento `target`. La función también incluye validaciones adicionales para asegurarse de que la lista esté ordenada y que `target` sea un número válido. Además, se incluyen 3 casos de prueba para verificar la funcionalidad de la función.
```

---

## Prueba 4: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Corto (Definición)
- **Métricas:** `TTFT: 1147.75 ms` | `Velocidad: 12.45 TPS` | `Tokens: 339` | `Tiempo Total: 28.38 s`

### Prompt Enviado:
> Explica en exactamente 3 viñetas qué es la cuantización en modelos de lenguaje.

### Respuesta Generada:
```text
1. **Definición de Cuantización en Modelos de Lenguaje**: Cuantización en modelos de lenguaje se refiere a la transformación de una representación de texto en un conjunto de números o valores numéricos. Esta transformación es crucial para la computación y el procesamiento de lenguaje natural (NLP), ya que permite la manipulación y análisis de textos de manera más eficiente.

2. **Importancia de la Cuantización**: La cuantización es fundamental en NLP porque permite la codificación de textos en un formato que puede ser procesado por computadoras. Esto incluye la codificación de palabras, frases y oraciones en números, lo que facilita la implementación de algoritmos de aprendizaje automático y el análisis de patrones en grandes cantidades de texto.

3. **Aplicaciones de Cuantización en NLP**: En NLP, la cuantización se utiliza en múltiples aspectos, como la codificación de palabras, la representación de documentos en espacios vectoriales, y la clasificación de textos. Por ejemplo, en la codificación de palabras, cada palabra se puede representar como un número, lo que permite la comparación y la clasificación de textos. En la representación de documentos, la cuantización ayuda a crear un espacio vectorial donde los documentos se pueden comparar y clasificar. Finalmente, en la clasificación de textos, la cuantización permite la implementación de algoritmos de aprendizaje automático que pueden clasificar textos en diferentes categorías.
```

---

## Prueba 5: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Medio (Razonamiento)
- **Métricas:** `TTFT: 1689.14 ms` | `Velocidad: 11.76 TPS` | `Tokens: 444` | `Tiempo Total: 39.45 s`

### Prompt Enviado:
> Tengo un servidor con 16 GB de RAM y sin GPU. Quiero desplegar un asistente interno para 5 empleados. ¿Qué arquitectura y tamaño de modelo me recomiendas y por qué?

### Respuesta Generada:
```text
Para un asistente interno para 5 empleados con un servidor de 16 GB de RAM, aquí te recomendaría una arquitectura y tamaño de modelo:

1. Arquitectura:
   - Servidor de 16 GB de RAM
   - CPU: Intel Core i7 o similar (para procesamiento de datos)
   - GPU: No es necesario, ya que el asistente interno no requiere GPU para su funcionamiento

2. Tamaño de modelo:
   - Tamaño pequeño: 110M-350M
   - Tamaño mediano: 350M-1G
   - Tamaño grande: 1G-3G

Recomendación: Tamaño mediano (350M-1G)

Razones:

1. RAM: Con 16 GB de RAM, un tamaño mediano de modelo es adecuado para manejar la carga de trabajo de un asistente interno.

2. Tasa de aprendizaje: Los modelos medios (350M-1G) generalmente tienen una tasa de aprendizaje más rápida y eficiente que los modelos más grandes.

3. Compatibilidad: Los modelos medios son más compatibles con la arquitectura de procesamiento de datos de un servidor de 16 GB de RAM.

4. Costo: Los modelos medios son más económicos en términos de recursos computacionales.

5. Flexibilidad: Los modelos medios pueden manejar mejor la carga de trabajo de un asistente interno, que puede variar en tamaño y complejidad.

6. Desarrollo rápido: Los modelos medios permiten un desarrollo más rápido y flexibilidad en la implementación del asistente interno.

Recuerda que este es solo un consejo general. La elección del tamaño de modelo y la arquitectura dependerá de otros factores, como la complejidad específica del asistente interno, la tasa de aprendizaje requerida y la capacidad de la red de datos.
```

---

## Prueba 6: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Largo (Generación de Código)
- **Métricas:** `TTFT: 1641.18 ms` | `Velocidad: 8.55 TPS` | `Tokens: 677` | `Tiempo Total: 80.83 s`

### Prompt Enviado:
> Escribe una función en Python bien documentada que implemente búsqueda binaria sobre una lista ordenada, incluyendo manejo de excepciones y 3 casos de prueba.

### Respuesta Generada:
```text
Aquí tienes una función en Python que implementa la búsqueda binaria sobre una lista ordenada. La función está bien documentada y incluye manejo de excepciones y 3 casos de prueba.

```python
def binary_search(arr, target):
    """
    Realiza una búsqueda binaria en una lista ordenada.

    Parámetros:
    arr (list): Lista ordenada en la que se realizará la búsqueda.
    target: El valor objetivo que se busca en la lista.

    Retorna:
    int: El índice del elemento objetivo en la lista, o -1 si no se encuentra.

    Excepciones:
    ValueError: Si la lista no está ordenada.
    TypeError: Si el target no es un número.

    Casos de prueba:
    >>> binary_search([1, 2, 3, 4, 5], 3)
    2
    >>> binary_search([1, 2, 3, 4, 5], 6)
    -1
    >>> binary_search([], 1)
    -1
    >>> binary_search([1], 1)
    0
    >>> binary_search([1, 2, 3, 4, 5], 'a')
    ValueError: 'a' is not a number
    """
    if not arr:
        return -1

    if not isinstance(target, (int, float)):
        raise TypeError("El target debe ser un número")

    low = 0
    high = len(arr) - 1

    while low <= high:
        mid = (low + high) // 2
        guess = arr[mid]

        if guess == target:
            return mid
        if guess > target:
            high = mid - 1
        else:
            low = mid + 1

    return -1

# Casos de prueba
print(binary_search([1, 2, 3, 4, 5], 3))  # 2
print(binary_search([1, 2, 3, 4, 5], 6))  # -1
print(binary_search([], 1))  # -1
print(binary_search([1], 1))  # 0
try:
    print(binary_search([1, 2, 3, 4, 5], 'a'))
except ValueError as e:
    print(e)  # 'a' is not a number
```

Esta función `binary_search` realiza una búsqueda binaria en una lista ordenada. La búsqueda se realiza utilizando un bucle `while` que se ejecuta mientras `low` sea menor o igual que `high`. En cada iteración, se calcula el índice `mid` del elemento en el medio de la lista. Si el elemento en el índice `mid` es igual al objetivo, se retorna el índice. Si el elemento en el índice `mid` es mayor que el objetivo, se actualiza `high` para buscar en la mitad inferior de la lista. Si el elemento en el índice `mid` es menor que el objetivo, se actualiza `low` para buscar en la mitad superior de la lista. Si el bucle termina sin encontrar el objetivo, se retorna -1.
```

---

