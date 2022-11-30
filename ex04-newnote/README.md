```
sequenceDiagram
browser->>server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
Note over server: server redirect to HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server->>browser: HTML-code

browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server->>browser: HTML-code
browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server->>browser: main.css
browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server->>browser: main.js

Note over browser: browser starts executing js-code that requests JSON data from server 

browser->>server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server->>browser: [{ content: "", date: "2022-11-30T03:09:42.453Z"}, ...]

Note over browser: browser executes the event handler that renders notes to display

browser->>server: HTTP GET https://studies.cs.helsinki.fi/favicon.ico
server->>browser: favicon.io
```