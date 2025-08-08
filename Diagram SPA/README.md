```mermaid
sequenceDiagram
    participant Usuário
    participant Navegador
    participant Servidor

    Usuário->>Navegador: 1. Acessa a URL
    Navegador->>Servidor: 2. GET /exampleapp/spa
    Servidor-->>Navegador: 3. Responde com HTML, CSS, e JS
    Navegador-->>Usuário: 4. Renderiza a UI
    Usuário->>Navegador: 5. Interage com a UI
    Navegador->>Servidor: 6. GET /notes (requisição de dados)
    Servidor-->>Navegador: 7. Responde com dados em JSON
    Navegador-->>Usuário: 8. Atualiza a UI (sem recarregar)