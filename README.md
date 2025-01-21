# Literalura - API de Libros con Spring Boot

Literalura es una aplicación basada en **Spring Boot** que interactúa con la API de [Gutendex](https://gutendex.com). Permite buscar libros por títulos, idiomas y autores, así como registrar el historial de búsquedas.

## Características principales

- **Búsqueda de libros por título**: Realiza búsquedas de libros según palabras clave en el título.
- **Filtrado por idioma**: Encuentra libros disponibles en un idioma específico.
- **Autores vivos en un año dado**: Consulta autores que estuvieron vivos en un año específico.
- **Historial de búsquedas**: Guarda y recupera las búsquedas realizadas por los usuarios.

## Tecnologías utilizadas

- **Java 17**
- **Spring Boot 3.x**
- **Gutendex API**
- **H2 Database** (opcional, para almacenamiento local de búsquedas)
- **Lombok** (para simplificar la gestión de modelos y DTOs)
- **Jackson** (para procesar JSON)
- **JUnit 5** para pruebas unitarias

## Configuración inicial

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/usuario/literalura.git
   cd literalura
# Properties

# Configuración de la API de Gutendex
gutendex.api.url=https://gutendex.com
# Puerto del servidor
server.port=8080
# bash
mvn clean install
mvn spring-boot:run

## Servicio principal: GutendexService

Gestiona las interacciones con la API externa.
Utiliza HttpClient para enviar solicitudes.
Serializa y deserializa datos con Jackson.
Guarda búsquedas en una base de datos usando SearchHistoryRepository.
Modelos y DTOs:

BookResponse: Representa la respuesta de la API de Gutendex.
Person: Representa la información de los autores.
Persistencia:

SearchHistory: Entidad que guarda el historial de búsquedas.

## Futuras mejoras
Implementar paginación en las respuestas de los endpoints.
Añadir autenticación para los usuarios.
