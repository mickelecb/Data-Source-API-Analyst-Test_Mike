# Troubleshooting Guide
--------------------------------Español-----------------------------------------------
Esta guía documenta los errores comunes encontrados durante la conexión con la API de GitHub y sus posibles soluciones.

---

## 1. Error 401 Unauthorized

**Causas posibles:**
- Token inválido, caducado o mal escrito.
- Falta de autorización en los headers.

**Solución:**
- Verifica el token personal.
- Asegúrate de que el header incluya:

## 2. Error 403 Rate Limit Exceeded

**Causas posibles:**
- Se hicieron más de 5000 peticiones por hora (con token).
- Se hicieron más de 60 peticiones por hora (sin token).

**Solución:**
- Leer el header `X-RateLimit-Remaining`.
- Si llega a 0, leer `X-RateLimit-Reset` y usar `time.sleep()` para esperar.

## 3. Paginación incompleta

**Resultado:**  
Solo se reciben 30 elementos, aunque hay más datos disponibles.

**Causas posibles:**
- No se especificaron `per_page` ni `page` en la URL.

**Solución:**
- Usar `?per_page=100&page=1`, `page=2`, etc.
- Implementar bucle hasta que no haya más resultados.

## Recomendaciones

- Autenticación con token.
- Manejo de cabeceras HTTP.
- Control de errores con `try/except`.
- Esperas dinámicas cuando se alcanza el rate limit.
- Guardado de resultados en formato JSON.

----------------------English----------------

# Troubleshooting Guide

This guide documents common errors encountered when connecting to the GitHub API and their possible solutions.

---

## 1. Error 401 Unauthorized

**Possible causes:**
- Invalid, expired, or incorrectly typed token.
- Missing authorization headers.

**Solution:**
- Verify your personal token.
- Ensure the request headers include:

Authorization: Bearer YOUR_TOKEN

## 2. Error 403 Rate Limit Exceeded

**Possible causes:**
- More than 5,000 requests per hour (with token).
- More than 60 requests per hour (without token).

**Solution:**
- Read the `X-RateLimit-Remaining` header.
- If it reaches 0, read `X-RateLimit-Reset` and use `time.sleep()` to wait.

---

## 3. Incomplete Pagination

**Symptom:**  
Only 30 items are received, even though more data is available.

**Possible causes:**
- The URL is missing `per_page` and `page` parameters.

**Solution:**
- Use `?per_page=100&page=1`, `page=2`, etc.
- Implement a loop until no more results are returned.

---

## Recommendations

- Use token-based authentication.
- Handle HTTP headers properly.
- Implement error handling with `try/except`.
- Add dynamic waits when the rate limit is reached.
- Save results in JSON format.
