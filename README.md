# Movies Application

This project is a simple Movies Application built with Spring Boot and MongoDB. It provides a RESTful API for managing movies and their reviews.

## Features

- Manage movies and their associated reviews.
- Store movie information such as title, release date, trailer link, poster, and genres.
- Retrieve a list of all movies or a single movie by its IMDb ID.
- Add reviews to movies.

## Technologies Used

- Java
- Spring Boot
- MongoDB
- Lombok

## Project Structure

The project consists of the following main components:

- `MoviesApplication`: The main class that bootstraps the Spring Boot application.
- `Movie`: The entity class representing a movie.
- `Review`: The entity class representing a review.
- `MovieController`: The REST controller for managing movies.
- `ReviewController`: The REST controller for managing reviews.
- `MovieService`: The service class for handling movie-related business logic.
- `ReviewService`: The service class for handling review-related business logic.
- `MovieRepository`: The repository interface for performing CRUD operations on movies.
- `ReviewRepository`: The repository interface for performing CRUD operations on reviews.

## Endpoints

### Movies

- `GET /api/v1/movies`: Retrieve a list of all movies.
- `GET /api/v1/movies/{imdbId}`: Retrieve a single movie by its IMDb ID.

### Reviews

- `POST /api/v1/reviews`: Create a new review.

## Getting Started

### Prerequisites

- Java 8 or later
- Maven
- MongoDB

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/movies-application.git
   ```
2. Navigate to the project directory:
   ```bash
   cd movies-application
   ```
3. Install the dependencies:
   ```bash
   mvn install
   ```
4. Run the application:
   ```bash
   mvn spring-boot:run
   ```

### Configuration

Ensure MongoDB is running on its default port (`27017`). If your MongoDB instance is running on a different host or port, you can configure it in the `application.properties` file located in the `src/main/resources` directory.

```properties
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=moviesdb
```

### Testing

You can test the API endpoints using tools like Postman or cURL.

#### Example: Retrieve All Movies

```bash
curl -X GET http://localhost:8080/api/v1/movies
```

#### Example: Retrieve a Single Movie by IMDb ID

```bash
curl -X GET http://localhost:8080/api/v1/movies/{imdbId}
```

#### Example: Create a New Review

```bash
curl -X POST http://localhost:8080/api/v1/reviews -H "Content-Type: application/json" -d '{"reviewBody": "Great movie!", "imdbId": "tt1234567"}'
```

## Lombok

This project uses Lombok to reduce boilerplate code. If you're using an IDE, make sure you have the Lombok plugin installed and enabled.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
