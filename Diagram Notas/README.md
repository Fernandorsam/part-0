

```mermaid
    sequenceDiagram
    participant browser
    participant server

    Note right of browser: O usuário digita uma nova nota no campo de texto e clica no botão "submit"
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server

    Note left of server: O servidor processa a nova nota, salva no banco de dados e adiciona a nova nota no final da lista de notas existente.
    server-->>browser: Redireciona para a página principal (HTTP 302)
    deactivate server

    Note right of browser: O navegador envia uma nova requisição GET para a URL https://studies.cs.helsinki.fi/exampleapp/notes
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
 
    server-->>browser: HTML document (incluindo a nova nota)
    deactivate server
    Note right of browser: O navegador renderiza a página HTML atualizada, exibindo a nova nota na lista.



    
