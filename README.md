# Proyecto-SQL

## Introducción

El proyecto se centra en el análisis de un conjunto de datos proveniente de un servicio emergente en el mercado de libros electrónicos. La pandemia de COVID-19 cambió los hábitos de las personas, llevando a un incremento en la lectura como actividad principal en casa. Esto atrajo la atención de startups que buscan soluciones innovadoras para los lectores.

El objetivo de este análisis es procesar los datos disponibles para generar una propuesta de valor para un nuevo producto en el sector. Se analizarán libros, editoriales, autores, calificaciones y reseñas de los usuarios para responder preguntas clave y extraer insights estratégicos.

---

## Objetivo Principal

Transformar los datos proporcionados en información útil para desarrollar y optimizar un producto competitivo para el mercado de lectura digital. Este análisis busca responder las siguientes preguntas:
1. ¿Cuántos libros fueron publicados después del 1 de enero de 2000?
2. ¿Cuántas reseñas de usuarios y cuál es la calificación promedio por cada libro?
3. ¿Cuál editorial ha publicado más libros con más de 50 páginas?
4. ¿Qué autor tiene la calificación promedio más alta entre libros con al menos 50 calificaciones?
5. ¿Cuál es el número promedio de reseñas de texto entre usuarios que han calificado más de 50 libros?

---

## Descripción de los Datos

### **books**
Contiene información sobre los libros, incluyendo:
- `book_id`: Identificación única del libro.
- `author_id`: Identificación del autor o autora.
- `title`: Título del libro.
- `num_pages`: Número de páginas del libro.
- `publication_date`: Fecha de publicación del libro.
- `publisher_id`: Identificación de la editorial.

### **authors**
Información sobre los autores:
- `author_id`: Identificación única del autor o autora.
- `author`: Nombre del autor o autora.

### **publishers**
Información sobre las editoriales:
- `publisher_id`: Identificación única de la editorial.
- `publisher`: Nombre de la editorial.

### **ratings**
Calificaciones de los usuarios:
- `rating_id`: Identificación única de la calificación.
- `book_id`: Identificación del libro calificado.
- `username`: Nombre del usuario que calificó.
- `rating`: Calificación asignada al libro (numérica).

### **reviews**
Reseñas de clientes:
- `review_id`: Identificación única de la reseña.
- `book_id`: Identificación del libro reseñado.
- `username`: Nombre del usuario que escribió la reseña.
- `text`: Contenido de la reseña.

---

## Pasos del Análisis

### 1. **Exploración y Preparación de los Datos**
- Cargar y revisar los datasets para entender su estructura.
- Limpiar los datos:
  - Convertir tipos de datos si es necesario.
  - Identificar y manejar valores ausentes o duplicados.
- Integrar tablas relevantes para conectar información (por ejemplo, combinar `books`, `authors` y `publishers`).

### 2. **Responder las Preguntas Clave**
1. **Libros publicados después del 1 de enero de 2000**:
   - Filtrar los libros según la columna `publication_date`.
2. **Reseñas y calificaciones promedio por libro**:
   - Contar el número de reseñas (`reviews`) y calcular la calificación promedio (`ratings`) por cada `book_id`.
3. **Editorial con más libros (>50 páginas)**:
   - Filtrar libros con más de 50 páginas y agrupar por `publisher_id` para identificar la editorial con más publicaciones.
4. **Autor con la calificación promedio más alta**:
   - Filtrar libros con al menos 50 calificaciones y calcular el promedio de calificaciones por autor (`author_id`).
5. **Promedio de reseñas por usuarios activos**:
   - Filtrar usuarios que calificaron más de 50 libros y calcular la cantidad promedio de reseñas de texto.

### 3. **Visualización de Resultados**
- Crear tablas resumidas y gráficos para representar los hallazgos:
  - Barras para el número de libros por editorial.
  - Distribuciones de calificaciones por autor.
  - Diagramas de dispersión para identificar tendencias en reseñas y calificaciones.

---

## Herramientas Recomendadas
- **Python**:
  - Manipulación de datos: `Pandas`.
  - Análisis y cálculos estadísticos: `NumPy`.
  - Visualización: `Matplotlib`, `Seaborn`.
- **Entorno**: Jupyter Notebook para una estructura clara y reproducible del análisis.

---

## Resultados Esperados
- Un informe detallado que responda las preguntas clave planteadas.
- Insights accionables para desarrollar una propuesta de valor competitiva.
- Visualizaciones claras que respalden las recomendaciones estratégicas.

---
## Conclusiones
El análisis de la base de datos proporcionada por el servicio emergente en el mercado literario digital ha revelado una serie de insights valiosos que pueden informar el desarrollo de una propuesta de valor sólida para una nueva aplicación de lectura. A continuación, se resumen los hallazgos más relevantes:

1. **Producción Editorial Activa**:
   - Desde el 1 de enero de 2000, se han publicado 819 libros, indicando una producción editorial robusta y adaptativa a las demandas cambiantes del mercado. Esto refleja la capacidad de las editoriales para mantenerse relevantes en tiempos de crisis y cambios globales, como lo fue la pandemia del coronavirus.

2. **Cantidad de reseñas por libro**:
   - La cantidad de reseñas por libro varía significativamente, desde una única reseña hasta cuatro reseñas en los ejemplos proporcionados. Esto sugiere que algunos libros tienen un mayor nivel de participación de los usuarios que otros, lo cual podría estar influenciado por factores como la popularidad del libro, la campaña de marketing y la accesibilidad..

3. **Calidad Literaria de Diana Gabaldon**:
   - Identificar a J.K. Rowling como el autor con la más alta calificación promedio proporciona una valiosa oportunidad para desarrollar estrategias de contenido y marketing que mejoren la experiencia del usuario y el éxito de la nueva aplicación. Los libros de J.K. Rowling, especialmente la serie de Harry Potter, no solo atraen a muchos lectores, sino que también son altamente valorados por ellos, indicando una base de seguidores leales y satisfechos.

4. **Compromiso de los Usuarios**:
   - Los usuarios que han calificado más de 50 libros han dejado un promedio de 24.33 reseñas de texto. Este alto nivel de participación y feedback cualitativo refleja una comunidad activa y comprometida, lo cual es un activo valioso para cualquier plataforma literaria.
