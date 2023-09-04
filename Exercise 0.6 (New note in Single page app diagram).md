```mermaid
sequenceDiagram
    participant browser
    participant server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server 
    server-->>browser: HTML document
    deactivate server 

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: The CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>browser: The JavaScript file
    deactivate server

    Note right of browser: User interacts with text field and posts new note
```