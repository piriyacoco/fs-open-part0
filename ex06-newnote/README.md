```mermaid
sequenceDiagram

browser->>server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
Note over browser: browser starts executing js-code that requests to add JSON data to data.json
Note over server: servers adds new note to data.json
server->>browser: JSON-data
```