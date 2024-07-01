```mermaid
  sequenceDiagram
      participant browser
      participant server
      browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
      server ->>browser : https://studies.cs.helsinki.fi/exampleapp/notes
      browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
      server-->>browser: HTML document
      browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
      server-->>browser: the css file
      browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
      server-->>browser: the Javascript file
      browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
      server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
```

sequenceDiagram
  participant browser
  participant server

  browser-->> server : POST https://studies.cs.helsinki.fi/exampleapp/new_note
  activate server 
  server-->> browser: https://studies.cs.helsinki.fi/exampleapp/notes
  deactivate server

   browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the css file
    deactivate server

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server
  
