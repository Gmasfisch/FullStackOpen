```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user writes a note and clicks Save. The JavaScript adds the note to the list and re-renders it on the page

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: The server saves the new note
    server-->>browser: 201 Created
    deactivate server
```
