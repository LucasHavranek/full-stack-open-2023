sequenceDiagram
    note over browser:
    user select text field and give input information
    click save button
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server-->>browser: HTML document

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server->>browser: css file

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server->>browser: Javascript file

    browser run javascript file and fetch json data from server
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>browser: [{ "content": "HTML é fácil", "date": "2023-1-1" },]
    browser run callback function which render notes

