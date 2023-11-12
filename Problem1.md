```mermaid

sequenceDiagram
    participant browser
    participant GitHub

    browser->>GitHub: POST https://api.github.com/repos/:user/:repo/issues (new issue data)
    activate GitHub
    GitHub-->>browser: 201 Created (issue created successfully)
    deactivate GitHub

    Note right of browser: Once the issue is created,<br/>the browser may update the view to show the new issue.
