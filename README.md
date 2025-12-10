# Microservices learning scaffold — user-service

Este repo es el punto de partida para aprender microservicios con:
- Java 21
- Spring Boot
- Gradle (Kotlin DSL)
- Lombok
- Spring Data JPA (H2 en memoria)
- YAML config
- Dockerfile

Cómo correr localmente:
1. En la raíz:
    - ./gradlew :user-service:bootRun
    - o para construir: ./gradlew :user-service:bootJar
2. Accede a:
    - API: http://localhost:8080/api/users
    - H2 console: http://localhost:8080/h2-console (JDBC URL: jdbc:h2:mem:usersdb)

Git + GitFlow (sugerencia):
- Inicializar repo:
    - git init
    - git add .
    - git commit -m "Initial scaffold: user-service"
- Instalar git-flow (opcional) y empezar:
    - git flow init
    - git flow feature start add-gateway
    - git flow feature finish add-gateway

Siguientes pasos recomendados:
1. Añadir un API Gateway (Spring Cloud Gateway).
2. Introducir service discovery / config server (Spring Cloud).
3. Integrar Keycloak para auth (OAuth2 / OpenID Connect).
4. Configurar CI (GitHub Actions) y calidad (SonarQube OSS, SpotBugs).
5. Construir imágenes Docker en CI y desplegar a minikube / kind o OpenShift.
