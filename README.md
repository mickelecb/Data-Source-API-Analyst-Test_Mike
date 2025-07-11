----------------------------English-------------------
# Data Source API Analyst Test

This repository contains the technical assignment for the **Data Source API Analyst** role.  
The goal is to demonstrate skills in API research, data extraction, error handling, and documentation.

---

##  Project Structure
### 1. GitHub API Research
- Identified key endpoints:
  - `/search/repositories`
  - `/repos/{owner}/{repo}/commits`
  - `/repos/{owner}/{repo}/contents/{path}`
- Reviewed documentation for authentication, pagination, rate limits, and errors.

### 2. API Extraction via Google Colab
- Configured authentication using a personal access token.
- Wrote Python code to extract data from GitHub API.
- Implemented pagination and rate limit handling.
- Saved results to a JSON file.

### 3. Error Handling
- Common issues and solutions documented in:  
  [`Content/troubleshooting.md`](Content/troubleshooting.md)

### 4. Final Output
- [`commits.json`](Content/commits.json): Extracted list of commits from the repository `dipucriodigital/engenharia-de-software`.
- [`github_api_colab.ipynb`](Content/Data_Source_Test.ipynb): Notebook with the complete code, including authentication, pagination, and error handling.

---

## 💡 Final Reflection

This test reinforced the importance of deeply understanding an API before implementation.  
It highlighted the need for:
- Strong error handling
- Efficient use of pagination and rate limits
- Clean and documented code

Google Colab proved to be an efficient and accessible platform for rapid API development and testing.

----------------------------Español-------------
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
- [Notebook en Colab](Content/Data_Source_Test.ipynb): Código completo con autenticación, paginación, rate limit y guardado de datos.

---

## 

Este ejercicio refuerza la importancia de entender la estructura y limitaciones de una API antes de interactuar con ella. Se destacó la necesidad de manejar errores, autenticarse correctamente y documentar el proceso de extracción de datos.



