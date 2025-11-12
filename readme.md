```mermaid
sequenceDiagram
  actor Alice as browser
  actor Bob as server

  
  Alice ->> Bob: post https://studies.cs.helsinki.fi/exampleapp/new_note
  activate server
  Bob -->> Alice: response 302 redirection /notes
  deactivate server
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/notes
  activate server
  Bob -->> Alice: HTML document
  deactivate server
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  Bob -->> Alice: css file
  deactivate server
  Alice->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/main.js
  activate server
  Bob -->> Alice: js file
  deactivate server
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  activate server
  Bob -->> Alice: [{"nombre":"Alice",...}...]
  deactivate server
```
