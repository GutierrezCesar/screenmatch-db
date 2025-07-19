# screenmatch-db

Proyecto basado en el curso de Alura, que consume datos de series desde la API de OMDb y los almacena en una base de datos usando Spring Data JPA. También se realiza procesamiento y consultas sobre los datos almacenados.

## 📦 Tecnologías utilizadas

- Java 17  
- Spring Boot  
- Spring Data JPA  
- H2 / PostgreSQL / MySQL (según configuración)  
- OMDb API  
- Docker (para conexión a la base de datos)  
- Maven  

## 🚀 Funcionalidades

- Buscar series por título desde la web (OMDb API)  
- Guardar series y episodios en base de datos  
- Consultar series por categoría  
- Mostrar top 5 series según evaluación  
- Filtrar series por temporada y evaluación mínima  
- Buscar episodios por nombre  
- Mostrar top 5 episodios de una serie  

## 🐳 Uso con Docker

Para ejecutar la base de datos usando Docker (ejemplo con PostgreSQL):

```bash
docker run --name screenmatch-db \
  -e POSTGRES_USER=usuario \
  -e POSTGRES_PASSWORD=clave \
  -e POSTGRES_DB=screenmatch \
  -p 5432:5432 \
  -d postgres
```
Luego asegúrate de configurar la conexión en application.properties o application.yml.

## 🔐 Variables de entorno

- Este proyecto requiere una API Key de OMDb para funcionar correctamente. 
- No incluyas claves directamente en el código.
- Usa variables de entorno o un archivo .env.
- String apiKey = System.getenv("OMDB_API_KEY");
