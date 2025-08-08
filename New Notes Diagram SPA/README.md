```mermaid
    sequenceDiagram
    participant Usuário
    participant Navegador
    participant Servidor
    participant BancoDeDados

    Usuário->>Navegador: 1. Digita a nova nota e clica em "Salvar"
    Navegador->>Servidor: 2. Requisição POST para /notes com dados da nota
    Servidor->>BancoDeDados: 3. Salva a nota
    BancoDeDados-->>Servidor: 4. Confirmação
    Servidor-->>Navegador: 5. Responde com dados da nova nota em JSON
    Navegador-->>Usuário: 6. Adiciona a nova nota à lista na UI (sem recarregar)