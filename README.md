# Frontend Spring Boot

Este diretório agora é um segundo projeto Spring Boot, separado do backend.

## Conteúdo
- `pom.xml`
- `src/main/java/com/seufronend/frontend/FrontendApplication.java`
- `src/main/resources/application.properties`
- `src/main/resources/static/index.html`
- `src/main/resources/static/style.css`
- `src/main/resources/static/script.js`

## Como rodar localmente
1. Inicie a API no diretório `projeto-frontend`:
   ```bash
   cd "c:\projeto frontend\projeto-frontend"
   .\mvnw spring-boot:run
   ```
   A API deve rodar em `http://localhost:8081`.

2. Inicie o frontend no diretório `frontend`:
   ```bash
   cd "c:\projeto frontend\frontend"
   ..\projeto-frontend\mvnw spring-boot:run
   ```
   O frontend deve rodar em `http://localhost:8080`.

## Configuração da API no frontend
O `frontend/src/main/resources/static/script.js` já está apontando para:
```js
const API_BASE_URL = 'http://localhost:8081/produtos';
```

## Deploy no Render
- Publique `projeto-frontend/` como um **Web Service** para a API.
- Publique `frontend/` como um **Web Service** para o frontend.
- Atualize `API_BASE_URL` no frontend para a URL pública da API no Render.
