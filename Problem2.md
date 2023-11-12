```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>browser: User creates a new note
    browser->>server: Form submit / POST request (new note data)
    activate server
    server-->>browser: HTML with updated note included
    deactivate server

    Note right of browser: Upon receiving the updated HTML,<br/>the browser refreshes the view to display the new note.
