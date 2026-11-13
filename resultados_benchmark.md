# Reporte de Benchmark y Respuestas: LLMOps Lab 1

Este documento detalla las respuestas completas obtenidas durante la evaluación de cuantización.

---

## Prueba 1: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Corto (Definición)
- **Métricas:** `TTFT: 492.03 ms` | `TPS: 19.97 tok/s` | `Total: 22.36 s` | `Tokens: 431`

### Prompt Enviado:
> Explica en exactamente 3 viñetas qué es la cuantización en modelos de lenguaje.

### Respuesta Generada:
```text
La cuantización en modelos de lenguaje es un concepto fundamental en la representación de la información en redes neuronales y, en particular, en los modelos de lenguaje como el Transformer. Aquí te explico en tres viñetas lo que es la cuantización:

1. **Representación de la información**: La cuantización implica la transformación de la información original en un espacio de representación más simple o reducido. En modelos de lenguaje, esto se refleja en la reducción de la cantidad de características o tokens que se utilizan para representar el texto. Por ejemplo, en un modelo de lenguaje tradicional, cada palabra o token puede tener una representación más compleja, pero en modelos cuantizados, se reduce a una representación más simple, como un número o una escala.

2. **Reducción de la complejidad**: La cuantización se realiza para reducir la complejidad computacional y matemática del modelo. En modelos cuantizados, se eliminan las operaciones matemáticas complejas y se sustituyen por operaciones más simples, como la suma o la multiplicación. Esto permite que los modelos sean más rápidos y más eficientes en términos de recursos computacionales.

3. **Ajuste de la precisión**: La cuantización también implica un ajuste en la precisión de la representación. En modelos cuantizados, se reduce la precisión de la representación de los datos, lo que puede llevar a una pérdida de información. Sin embargo, esta pérdida de precisión se compensa en la capacidad de generalización del modelo, ya que los modelos cuantizados pueden aprender patrones más robustos y generalizados a partir de datos más reducidos.

En resumen, la cuantización en modelos de lenguaje es una técnica que permite la representación de la información en un espacio más simple y reducido, a la vez que mejora la eficiencia computacional y la capacidad de generalización del modelo.
```

---

## Prueba 2: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Medio (Razonamiento)
- **Métricas:** `TTFT: 1996.67 ms` | `TPS: 16.42 tok/s` | `Total: 50.92 s` | `Tokens: 801`

### Prompt Enviado:
> Tengo un servidor con 16 GB de RAM y sin GPU. Quiero desplegar un asistente interno para 5 empleados. ¿Qué arquitectura y tamaño de modelo me recomiendas y por qué?

### Respuesta Generada:
```text
Para un servidor con 16 GB de RAM y sin GPU, la elección del modelo de asistente interno dependerá de varios factores, incluyendo la complejidad del trabajo que se realizará, la cantidad de información que se manejará y la precisión requerida. Aquí te dejo algunas recomendaciones basadas en la mayoría de los casos:

1. **Modelo de Asistente Interno:**
   - **Modelo de Conversación**: Si el trabajo principal es la conversación y la interacción con el usuario, podría considerar un modelo de conversación como Claude, Anthropic, o Anthropic. Estos modelos son diseñados para la interacción natural y la conversación, lo que podría ser adecuado para un asistente interno.
   - **Modelo de Inteligencia Artificial**: Si el trabajo principal es la toma de decisiones basada en datos, podría considerar un modelo de inteligencia artificial como Claude, Anthropic, o Anthropic. Estos modelos son diseñados para la toma de decisiones basadas en datos y pueden ser adecuados para un asistente interno.

2. **Tamaño de Modelo:**
   - **Modelo de Conversación**: Para un asistente interno de conversación, podría considerar un modelo de tamaño mediano a grande, como Claude o Anthropic. Estos modelos son generalmente más complejos y requieren más RAM, pero también pueden manejar más información y realizar más tareas.
   - **Modelo de Inteligencia Artificial**: Para un asistente interno de inteligencia artificial, podría considerar un modelo de tamaño mediano a grande, como Claude o Anthropic. Estos modelos son generalmente más complejos y requieren más RAM, pero también pueden manejar más información y realizar más tareas.

3. **Tamaño de la Base de Datos:**
   - **Modelo de Conversación**: Para un asistente interno de conversación, la base de datos podría ser más grande, ya que necesitará almacenar más información sobre las conversaciones y las interacciones del usuario.
   - **Modelo de Inteligencia Artificial**: Para un asistente interno de inteligencia artificial, la base de datos podría ser más grande, ya que necesitará almacenar más información sobre las decisiones y las tomas de decisiones basadas en datos.

4. **Tamaño de la Base de Datos:**
   - **Modelo de Conversación**: La base de datos de la conversación podría ser más grande, ya que necesitará almacenar más información sobre las conversaciones y las interacciones del usuario.
   - **Modelo de Inteligencia Artificial**: La base de datos de la inteligencia artificial podría ser más grande, ya que necesitará almacenar más información sobre las decisiones y las tomas de decisiones basadas en datos.

5. **Tamaño de la Base de Datos:**
   - **Modelo de Conversación**: La base de datos de la conversación podría ser más grande, ya que necesitará almacenar más información sobre las conversaciones y las interacciones del usuario.
   - **Modelo de Inteligencia Artificial**: La base de datos de la inteligencia artificial podría ser más grande, ya que necesitará almacenar más información sobre las decisiones y las tomas de decisiones basadas en datos.

En resumen, si el trabajo principal es la conversación, podría considerar un modelo de conversación como Claude o Anthropic. Si el trabajo principal es la toma de decisiones basadas en datos, podría considerar un modelo de inteligencia artificial como Claude o Anthropic. Ambos modelos son generalmente más complejos y requieren más RAM, pero también pueden manejar más información y realizar más tareas.
```

---

## Prueba 3: qwen2.5:1.5b-instruct-q4_K_M

- **Categoría de Prompt:** Largo (Generación de Código)
- **Métricas:** `TTFT: 1494.55 ms` | `TPS: 18.82 tok/s` | `Total: 31.8 s` | `Tokens: 569`

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
    target: El elemento objetivo a buscar en la lista.
    
    Retorna:
    int: El índice del elemento 'target' si se encuentra en la lista, -1 si no se encuentra.
    
    Excepciones:
    ValueError: Si la lista no está ordenada.
    TypeError: Si 'target' no es un número.
    """
    # Verificar si la lista está ordenada
    if not arr:
        raise ValueError("La lista no puede estar vacía.")
    
    # Verificar si 'target' es un número
    if not isinstance(target, (int, float)):
        raise TypeError("El target debe ser un número.")
    
    # Verificar si 'target' es menor que el primer elemento o mayor que el último elemento
    if target < arr[0] or target > arr[-1]:
        return -1
    
    # Realizar la búsqueda binaria
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    
    return -1

# Casos de prueba
print(binary_search([1, 2, 3, 4, 5], 3))  # Devuelve 2
print(binary_search([1, 2, 3, 4, 5], 6))  # Devuelve -1
print(binary_search([], 1))  # Lanza ValueError
print(binary_search([1, 2, 3, 4, 5], 'a'))  # Lanza TypeError
```

Esta función `binary_search` realiza una búsqueda binaria en una lista ordenada para encontrar el índice del elemento `target`. La búsqueda se realiza de manera eficiente, tomando en cuenta el hecho de que la lista está ordenada. Si el `target` se encuentra en la lista, la función devuelve su índice. Si el `target` no se encuentra, devuelve -1. La función también incluye manejo de excepciones para casos específicos como si la lista no está ordenada o si el `target` no es un número válido.
```

---

## Prueba 4: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Corto (Definición)
- **Métricas:** `TTFT: 758.79 ms` | `TPS: 14.17 tok/s` | `Total: 24.35 s` | `Tokens: 333`

### Prompt Enviado:
> Explica en exactamente 3 viñetas qué es la cuantización en modelos de lenguaje.

### Respuesta Generada:
```text
1. **Definición y Concepto**: La cuantización en modelos de lenguaje es un proceso que reduce la cantidad de información necesaria para representar una frase o texto. En términos técnicos, se refiere a la simplificación de una representación de texto en un conjunto de símbolos más reducido, como números o letras, que pueden ser interpretados de manera más eficiente.

2. **Aplicaciones y Beneficios**: Esta técnica es comúnmente utilizada en la codificación de texto, donde se reduce el tamaño de la codificación para mejorar la eficiencia de la transmisión o almacenamiento de datos. Además, en el procesamiento de lenguaje natural, la cuantización puede ayudar a simplificar la representación de oraciones y frases, lo que puede mejorar la precisión y la eficiencia de las aplicaciones de IA que utilizan este tipo de modelos.

3. **Impacto en la Precisión**: La cuantización puede tener un impacto significativo en la precisión de los modelos de lenguaje. Al reducir la cantidad de información necesaria para representar una frase, se pueden mejorar las capacidades de reconocimiento y predicción de palabras y oraciones, lo que puede mejorar la calidad del lenguaje natural y la eficacia de las aplicaciones de IA que utilizan estos modelos. Sin embargo, también es importante tener en cuenta que la reducción de información puede afectar la calidad del lenguaje, ya que puede limitar la flexibilidad y la complejidad de las representaciones.
```

---

## Prueba 5: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Medio (Razonamiento)
- **Métricas:** `TTFT: 1858.99 ms` | `TPS: 12.67 tok/s` | `Total: 41.21 s` | `Tokens: 497`

### Prompt Enviado:
> Tengo un servidor con 16 GB de RAM y sin GPU. Quiero desplegar un asistente interno para 5 empleados. ¿Qué arquitectura y tamaño de modelo me recomiendas y por qué?

### Respuesta Generada:
```text
Para un asistente interno para 5 empleados con un servidor de 16 GB de RAM, aquí te recomendaría una arquitectura y tamaño de modelo:

1. Arquitectura:
   - Servidor de 16 GB de RAM
   - CPU: Intel Core i7 o similar (para procesamiento de alto rendimiento)
   - GPU: No necesaria, ya que el asistente interno no requiere GPU para su funcionamiento

2. Tamaño de modelo:
   - Modelo pequeño: 110M-350M de parámetros
   - Modelo mediano: 350M-1G de parámetros
   - Modelo grande: 1G-3G de parámetros

Recomendación:
- Tamaño de modelo mediano: 350M-1G de parámetros
- Arquitectura: Servidor de 16 GB de RAM con CPU Intel Core i7

Razones:

1. RAM: El tamaño de modelo mediano es adecuado para un servidor de 16 GB de RAM, ya que permite un uso eficiente de la memoria RAM.

2. CPU: El CPU Intel Core i7 es adecuado para procesar el trabajo de un asistente interno, ya que puede manejar tareas de alto rendimiento.

3. Tamaño de modelo: Un modelo mediano es el más adecuado para un asistente interno, ya que proporciona un equilibrio entre rendimiento y capacidad de procesamiento.

4. Costo: Un modelo mediano es más económico que un modelo grande, lo que es beneficioso si tienes un presupuesto limitado.

5. Flexibilidad: Un modelo mediano permite una mayor flexibilidad en términos de personalización y actualizaciones, lo que puede ser útil si necesitas adaptar el asistente a las necesidades específicas de tus empleados.

6. Compatibilidad: Un modelo mediano es más compatible con la mayoría de las plataformas y entornos de trabajo, lo que facilita la integración y la colaboración.

Recuerda que estos son solo recomendaciones generales. La elección final dependerá de tus necesidades específicas, el tipo de trabajo que realizarán tus empleados y otros factores.
```

---

## Prueba 6: qwen2.5:1.5b-instruct-q8_0

- **Categoría de Prompt:** Largo (Generación de Código)
- **Métricas:** `TTFT: 1671.34 ms` | `TPS: 11.95 tok/s` | `Total: 68.32 s` | `Tokens: 794`

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
    arr (list): Lista ordenada en que se realizará la búsqueda.
    target: El valor objetivo que se busca en la lista.

    Retorna:
    int: El índice del elemento objetivo en la lista, si se encuentra. -1 si no se encuentra.

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
if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

### Explicación de la función:
1. **Entrada**: La función `binary_search` recibe dos parámetros: `arr` (una lista ordenada) y `target` (un número objetivo).
2. **Validación de entrada**: 
   - Verifica si la lista está vacía y devuelve `-1` si es así.
   - Verifica si el `target` es un número y lo convierte a un tipo numérico si no lo es.
3. **Búsqueda binaria**:
   - Inicializa `left` en el índice 0 y `right` en el índice último de la lista.
   - Mientras `left` sea menor o igual que `right`:
     - Calcula el índice `mid` como la mitad de `left` y `right`.
     - Compara `arr[mid]` con `target`:
       - Si `arr[mid]` es igual a `target`, devuelve `mid`.
       - Si `arr[mid]` es menor que `target`, mueve `left` a `mid + 1`.
       - Si `arr[mid]` es mayor que `target`, mueve `right` a `mid - 1`.
4. **Excepciones**:
   - Si la lista no está ordenada, lanza una excepción de tipo `ValueError`.
   - Si el `target` no es un número, lanza una excepción de tipo `TypeError`.
5. **Casos de prueba**: 
   - Utiliza `doctest.testmod()` para ejecutar los casos de prueba y asegurarse de que la función funcione correctamente.

Este código proporciona una implementación clara y documentada de la búsqueda binaria, incluyendo validaciones y casos de prueba para asegurar su correcto funcionamiento.
```

---

