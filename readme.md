``` sequenceDiagram
  actor Alice as browser
  actor Bob as server

  Alice ->> Bob: post https://studies.cs.helsinki.fi/exampleapp/new_note
  Bob ->> Alice: response 302 redirection /notes
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/notes
  Bob ->> Alice: HTML document
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  Bob ->> Alice: css file
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/main.js
  Bob ->> Alice: js file
  Alice ->> Bob: GET https://studies.cs.helsinki.fi/exampleapp/data.json
  Bob ->> Alice: [{"nombre":"Alice",...}...]
```
