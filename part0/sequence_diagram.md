sequenceDiagram

participant browser
participant server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/note
activate server
server-->>browser: 200(OK): text/html
deactivate server

browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note \n{note: "hello"}
activate server
server-->>browser: 304(Found): text/html
deactivate server
