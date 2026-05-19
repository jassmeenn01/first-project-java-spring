# Task 1 – Spring boot project

## Project Info

| Field        | Value                                      |
|--------------|--------------------------------------------|
| Group        | pl.edu.vistula                             |
| Artifact     | first-project-java-spring                  |
| Package      | pl.edu.vistula.first_project_java_spring   |
| Java Version | 21                                         |
| Spring Boot  | 3.5.14                                     |
| Build Tool   | Maven                                      |

---

## What This Project Does

This is a simple Spring Boot web application that demonstrates how to serve web content using Spring MVC. It covers:

- Creating a basic REST endpoint using `@RestController`
- Serving dynamic HTML pages using `@Controller` and Thymeleaf templates
- Passing data from a controller to a view using `Model`
- Reading URL parameters using `@RequestParam`
- Understanding the difference between `@RestController` and `@Controller` with `@ResponseBody`

---

## Dependencies

| Dependency   | Purpose                                      |
|--------------|----------------------------------------------|
| Spring Web   | Building web and RESTful applications        |
| Thymeleaf    | Server-side HTML template engine             |
| Lombok       | Reduces boilerplate Java code                |

---

## Project Structure

```
src/
└── main/
    ├── java/
    │   └── pl/edu/vistula/first_project_java_spring/
    │       ├── FirstProjectJavaSpringApplication.java   ← Main entry point
    │       └── controller/
    │           └── HelloController.java                 ← Web controller
    └── resources/
        ├── templates/
        │   └── greeting.html                           ← Thymeleaf HTML template
        ├── static/
        │   └── images/
        │       └── vistula.png                         ← Static image asset
        └── application.properties
```

---

## Endpoints

| URL                                      | Method | Description                              |
|------------------------------------------|--------|------------------------------------------|
| `http://localhost:8080/`                 | GET    | Returns a plain text greeting message    |
| `http://localhost:8080/greeting`         | GET    | Returns HTML page with default name      |
| `http://localhost:8080/greeting?name=Vistula` | GET | Returns HTML page with custom name  |

---

## How to Run

1. Make sure **Java 21** is installed
2. Clone or open the project in **IntelliJ IDEA**
3. Run `FirstProjectJavaSpringApplication.java`
4. Open your browser and go to `http://localhost:8080`

---

## Key Concepts 

**`@RestController`** — Combines `@Controller` and `@ResponseBody`. Returns data (text/JSON) directly in the response body, not an HTML page.

**`@Controller`** — Used when returning HTML views (Thymeleaf templates). Needs `@ResponseBody` on individual methods if you want to return plain text.

**`@GetMapping`** — Maps HTTP GET requests to a specific method. The `value` parameter defines the URL path.

**`@RequestParam`** — Reads a parameter from the URL (e.g. `?name=Vistula`). Can have a default value if not provided.

**`Model`** — An object used to pass data from the controller to the HTML template.

**Thymeleaf** — A template engine that allows dynamic content in HTML using `th:` attributes (e.g. `th:text`, `th:src`).

---

## Output
Visiting `http://localhost:8080/` renders:

<img width="653" height="267" alt="image" src="https://github.com/user-attachments/assets/a3058bfa-e2ac-4fd6-886f-a9a177cb0807" />

Visiting `http://localhost:8080/greeting?name=Vistula` renders:

<img width="871" height="908" alt="image" src="https://github.com/user-attachments/assets/1b4bdc08-5a63-49f2-81e4-c6d9de86b653" />


---

## Author

Jasmeen Kaur — Vistula University  
Spring Boot Basics — Task 1
