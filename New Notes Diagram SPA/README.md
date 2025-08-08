```mermaid

    A[Usuário] -->|1. Digita a nova nota e clica em "Salvar"| B(Navegador)
    B -->|2. Requisição POST para /notes| C[Servidor (API)]
    C -->|3. Salva a nova nota no banco de dados| D((Banco de Dados))
    D -->|4. Retorna confirmação e dados da nova nota em JSON| C
    C -->|5. Resposta em JSON (status 201 Created)| B
    B -->|6. Código JS adiciona a nova nota à lista na UI| A