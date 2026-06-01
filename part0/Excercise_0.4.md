```mermaid
sequenceDiagram

participant browser
participant server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/note
activate server
server-->>browser: notes.html, main.css, main.js,<br>data.json
deactivate server

browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note <br>{note: "hello"}
activate server
server-->>browser: new_note.html, main.css, main.js,<br>data.json
deactivate server
```
