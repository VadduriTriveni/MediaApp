### 🎵 Media Playlist App using Spring Boot

A media playlist management system built with **Spring Boot**, featuring RESTful API endpoints for managing playlists, songs, and integrating with **Swagger UI** for API documentation.

---

### 🚀 Features

* ✅ **Create, Update, Delete, and Retrieve Playlists** with CRUD operations.
* ✅ **Add, Remove, and Move Songs** between playlists.
* ✅ **Swagger UI** for API documentation and interaction.
* ✅ **Exception Handling** with custom error messages.
* ✅ **Database-backed** using JPA repositories with custom queries.
* ✅ **Spring Boot** framework for scalable backend development.

---

### 🛠️ Installation & Setup

#### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/MediaPlaylistApp.git
cd MediaPlaylistApp
```

#### 2. Set Up Dependencies

Install dependencies (Spring Boot starter dependencies included in the `pom.xml`):

```bash
mvn install
```

#### 3. Run the Application

You can run the Spring Boot application via:

```bash
mvn spring-boot:run
```

Alternatively, build and run the app as a JAR file:

```bash
mvn clean package
java -jar target/MediaPlaylistApp.jar
```

---

### 🧠 How It Works

1. **Playlist Management**:

   * **Create a Playlist** by specifying a name.
   * **Retrieve Playlists** by ID or list all playlists.
   * **Delete Playlists** using the playlist ID.

2. **Song Management**:

   * **Add Songs** to a specific playlist.
   * **Move Songs** between playlists.
   * **Delete Songs** from a playlist.

3. **API Documentation**: Use Swagger UI for easy API interaction at `http://localhost:8080/swagger-ui.html`.

---

### 💬 API Endpoints

#### Playlist Management

* **GET /playlist/all**: Retrieve all playlists.
* **GET /playlist/{id}**: Retrieve playlist by ID.
* **POST /playlist/{name}**: Create a new playlist.
* **DELETE /playlist/{id}**: Delete a playlist by ID.
* **GET /playlist/{id}/songs**: Get all songs in a playlist.
* **DELETE /playlist/{id}/songs**: Delete all songs from a playlist.

#### Song Management

* **POST /playlist/{id}/add**: Add a song to a playlist.
* **DELETE /playlist/{id}/songs/{song_id}**: Delete a specific song from a playlist.
* **PUT /songs/{id}/move**: Move a song to another playlist.
* **GET /songs**: Retrieve all songs across playlists.

---

### 🔐 Configuration

Ensure the application is properly configured in `application.properties`:

```properties
# H2 Database (for development)
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
```

### 🤖 Technology Stack

* **Spring Boot**: Simplified configuration and application setup.
* **Spring Data JPA**: Database access with JPA Repositories.
* **Swagger UI**: For interactive API documentation.
* **H2 Database**: Lightweight, in-memory database for fast development.

---

### 📌 Requirements

* Java 8 or higher
* Maven or Gradle for dependency management
* Spring Boot 2.x+

---

### ⚡ How to Use

1. Start the app and navigate to `http://localhost:8080/swagger-ui.html` for API documentation and to test the endpoints interactively.
2. Use Postman or any HTTP client to make requests to the API, such as:

   * **Create Playlist**: `POST /playlist/{name}`
   * **Add Song to Playlist**: `POST /playlist/{id}/add`
   * **Move Song to Another Playlist**: `PUT /songs/{id}/move?to_playlist={to_playlist_id}`

---

### 🎤 Example Usage

#### Create a Playlist

```bash
POST /playlist/MyPlaylist
```

#### Add a Song to Playlist

```bash
POST /playlist/{id}/add
{
    "name": "Song 1",
    "coverUrl": "http://example.com/song1.jpg"
}
```

#### Move a Song to Another Playlist

```bash
PUT /songs/{id}/move?to_playlist={new_playlist_id}
```

---

### 🙌 Acknowledgements

Thanks to the following technologies and libraries:

* [Spring Boot](https://spring.io/projects/spring-boot)
* [Swagger UI](https://swagger.io/tools/swagger-ui/)
* [H2 Database](https://www.h2database.com/html/main.html)
