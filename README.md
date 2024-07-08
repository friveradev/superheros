# Deployment Challenge
## Key Information:
* Consider the following environment variables:
  * SPRING_PROFILES_ACTIVE=prod
  * SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/superheroes
  * SPRING_DATASOURCE_USERNAME=username
  * SPRING_DATASOURCE_PASSWORD=password
* The API was built using MySQL 8 database.
* It should be compiled with Maven (mvn clean package) and then execute the .jar file

# Desafío de despliegue
## Datos a tener en cuenta:
* Tener en cuenta las variables de entorno:
  * SPRING_PROFILES_ACTIVE=prod
  * SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/superheroes
  * SPRING_DATASOURCE_USERNAME=username
  * SPRING_DATASOURCE_PASSWORD=password
* La API se creó con base de datos MySQL 8
* Se debe compilar con maven (mvn clean package) y luego ejecutar el .jar

---

# Superheroes API
## Description:
This API provides a way to manage a list of superheroes with their names, civil names, affiliations, abilities, and origin. It offers endpoints to retrieve all superheroes, search by name, retrieve a superhero by id, create a new superhero, update a superhero, and delete a superhero.

## Endpoints:
* ##### GET /api/superheroes: Returns all superheroes. Accepts an optional query parameter to filter by name. Returns a JSON array of superhero objects.
* ##### GET /api/superheroes/{id}: Returns the superhero with the specified id. Returns a JSON object with the superhero's properties.
* ##### POST /api/superheroes: Creates a new superhero. Accepts a JSON object with the superhero's properties (name, civil name, affiliation, abilities, and origin). Returns the newly created superhero object.
* ##### PUT /api/superheroes/{id}: Updates an existing superhero. Accepts a JSON object with the superhero's properties. Returns the updated superhero object.
* ##### DELETE /api/superheroes/{id}: Deletes the superhero with the specified id. Returns no content.

## Query Parameters:
name: Optional. Filters the list of superheroes by name. The parameter value is a string.

## Response Body
An array of superhero objects, each with the following fields:

* id: the ID of the superhero.
* name: the name of the superhero.
* civilName: the civil name of the superhero.
* comic: the comic of the superhero.
* powers: an array of powers possessed by the superhero.
* origin: the origin of the superhero.
* description: the description of the superhero.

## Example

```json
{
  "id": 1,
  "name": "Superman",
  "civilName": "Clark Kent",
  "comic": "DC Comics",
  "powers": [
    "Super strength",
    "Super speed",
    "Flight"
  ],
  "origin": "Krypton",
  "description": "Superman is a superhero with incredible strength, speed, and various other superpowers. He was sent to Earth from the planet Krypton and raised as Clark Kent in Smallville, Kansas. As Superman, he fights for truth, justice, and the American way."
}
```

## Swagger
[http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

## Authentication:
The API is not authenticated, but you can implement authentication using Spring Security or any other authentication method you prefer.

## Conclusion:
The Superheroes API provides a way to manage a list of superheroes with basic CRUD operations. With the optional name filter, clients can easily search and retrieve a subset of superheroes. Adding authentication and rate limiting can improve the security and stability of the API. Lastly, versioning can be implemented to ensure backward compatibility and smooth transitions to new API versions.