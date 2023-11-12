# Ejemplo de diagrama de secuencia con Mermaid

```mermaid
sequenceDiagram
    participant navegador
    participant servidor

    navegador->>servidor: POST https://studies.cs.helsinki.fi/exampleapp/notes (nuevos datos de nota)
    activate servidor
    servidor-->>navegador: 201 Creado (respuesta que confirma la creación exitosa)
    deactivate servidor

    Note right of navegador: Una vez que se crea la nota, el navegador se actualiza<br/>y potencialmente actualiza la vista para mostrar la nueva nota.
