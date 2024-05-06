Here is a simple flow chart:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: note information
    deactivate server

    Note right of browser: The server return the new note's information to browser to indicate the new note is created successfully.

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: all notes
    deactivate server

    Note right of browser: The browser fetch all notes from the server, then show them on the screen.

```
