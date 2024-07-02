```mermaid
  sequenceDiagram
      participant browser
      participant server
      browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
      server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
```
