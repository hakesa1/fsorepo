sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: response 201 created
    deactivate server

    Javascript code (which is executed in browser) gets form element and registers event handler.
    Code creates note and sends it to notes list.
    Code redraws notes.
    Code sends note to server.