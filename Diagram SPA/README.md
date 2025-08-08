```mermaid
    A -->|Requisição Inicial| B
    B -->|GET https://studies.cs.helsinki.fi/exampleapp/spa| C
    C -->|HTML, CSS, JS| B
    B -->|Renderiza a UI| A
    A -->|Interage com a UI| B
    B -->|Requisição de Notas POST/GET| C
    C -->|Retorna dados em JSON| B
    B -->|Atualiza a UI (sem recarregar a página)| A