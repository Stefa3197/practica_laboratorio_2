# Entregable Laboratorio 1: Benchmarking de Serving Local y Cuantización

- **Curso:** LLMOps, Serving Local y Arquitecturas RAG
- **Estudiante:** Estefani Muñoz Dorado
- **Hardware Utilizado:** 12th Gen Intel(R) Core(TM) i5-1235U / 7.71 GB RAM / Windows 10 Pro
- **Fecha:** 13 de noviembre de 2026

---

## Análisis Técnico de Resultados

### 1. Impacto en Memoria (MEM USAGE y KV Cache)
> ¿Cuál fue la diferencia exacta en MB/GB de RAM consumida entre `q4_K_M` y `q8_0` al ejecutar `docker stats`? ¿Por qué el consumo en ejecución supera el tamaño del archivo en disco?

**Respuesta:**
Al medir con docker stats, el modelo de 4 bits (qwen2.5:1.5b-instruct-q4_K_M) consumió 1.607 GiB (43.66 % del límite de 3.68 GiB), mientras que el modelo de 8 bits (qwen2.5:1.5b-instruct-q8_0) consumió 2.114 GiB (57.43 %). La diferencia exacta entre ambos es de 0.507 GiB (aproximadamente 519 MiB), lo que significa que q8_0 requiere un 31.5 % más de memoria RAM (o un ahorro del 24.0 % al emplear q4_K_M).

---

### 2. Ancho de Banda de Memoria y Velocidad (TPS)
> En inferencia sobre CPU, el cuello de botella suele ser el ancho de banda de la memoria RAM. ¿En qué porcentaje aumentó la velocidad (TPS) al pasar de 8 bits a 4 bits?

**Respuesta:**
Según las pruebas realizadas en CPU (Intel Core i5-1235U), la velocidad promedio aumentó en un 42.3 % al pasar de 8 bits a 4 bits

---

### 3. Latencia Inicial (TTFT) y Fase Prefill
> ¿Por qué el `TTFT (ms)` es significativamente más alto en el Prompt Largo que en el Prompt Corto?

**Respuesta:**
En mis resultados, el Time To First Token (TTFT) pasó de 492.03 ms a 1494.55 ms en q4_K_M  y de 758.79 ms a 1671.34 ms en q8_0. al comparar el prompt corto contra el prompt largo.

---

### 4. Calidad vs. Eficiencia en `resultados_benchmark.md`
> Revisando las 6 respuestas completas generadas, ¿hubo alguna degradación perceptible en la lógica del código Python o en el razonamiento generado por el modelo de 4 bits frente al de 8 bits?

**Respuesta:**
Para este modelo de 1.5B parámetros en CPU, la cuantización q4_K_M ofrece el mejor equilibrio producción/costo, logrando un 42.3 % más de velocidad y un 24.0 % menos de consumo de RAM sin sacrificar precisión práctica en tareas de código o razonamiento.

---
*Nota: Adjuntar junto con este documento los archivos generados `resultados_benchmark.csv` y `resultados_benchmark.md`.*
