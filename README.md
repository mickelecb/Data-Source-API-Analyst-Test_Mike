# Data Source API Analyst Test

Este proyecto es parte de una prueba técnica para el rol de **Data Source API Analyst**. El objetivo fue demostrar habilidades en el uso de APIs públicas, manejo de datos y resolución de errores comunes.

---

## 📌 Estructura del proyecto


---

### 1. Investigación de la API de GitHub
Se identificaron los siguientes endpoints:
- `/search/repositories`
- `/repos/{owner}/{repo}/commits`
- `/repos/{owner}/{repo}/contents/{path}`

### 2. Extracción de datos desde Colab
Se usó Google Colab con autenticación mediante token personal.  
Se implementó paginación, manejo de límites de peticiones (rate limit) y exportación de resultados.

### 3. Manejo de errores comunes
Ver archivo: [`Content/troubleshooting.md`](Content/troubleshooting.md)

### 4. Resultados
- [commits.json](Content/commits.json): Lista de commits extraída del repositorio `dipucriodigital/engenharia-de-software`.
- [Notebook en Colab](Content/github_api_colab.ipynb): Código completo con autenticación, paginación, rate limit y guardado de datos.

---

## 

Este ejercicio refuerza la importancia de entender la estructura y limitaciones de una API antes de interactuar con ella. Se destacó la necesidad de manejar errores, autenticarse correctamente y documentar el proceso de extracción de datos.

