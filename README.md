# MinSSG

MinSSG is an online static code-sharing platform that allows users to showcase project structures directly from a markdown file. With this tool, you can present your project’s folder structure, code snippets, and individual files in an interactive, static format. 

## Features
- Display project structure with tree view.
- Render code files from markdown with appropriate syntax highlighting.
- Easy-to-use markdown template to get started.

## Usage Instructions

1. Clone the repository:
    ```bash
    git clone <repository_url>
    cd MinSSG
    ```
2. Install the required dependencies:
    ```bash
    npm install
    ```
3. Run the application:
    ```bash
    npm start
    ```
4. To use MinSSG, create or modify the markdown file to include your project’s structure and code snippets. See the template below for an example.

## Project Structure

### Writing the Markdown

To get started with your markdown, follow this template. This template includes both a project structure and some sample code for each file.

### Example Markdown Template

```markdown
# Project Structure
- MyProject/
  - frontend/
    - src/
      - app/
        - main-page/
          - page.js
          - layout.ts
          - page.jsx
        - components/
          - button.tsx
  - backend/
    - api/
      - postman.json
    - servers/
      - server.py
      - server-lite.py


## MyProject/frontend/src/app/main-page/page.js

```js
// Example JavaScript code
function HelloWorld() {
  return <h1>Hello, world!</h1>;
}

export default HelloWorld;



## MyProject/frontend/src/app/layout.ts

```ts
// Example TypeScript code
import React from 'react';

const Layout: React.FC = ({ children }) => {
  return <div className="layout">{children}</div>;
};

export default Layout;


## MyProject/frontend/src/app/page.jsx

```jsx
// Example JSX code
import React from 'react';
import HelloWorld from './main-page/page.js';

function Page() {
  return (
    <div>
      <HelloWorld />
    </div>
  );
}

export default Page;


## MyProject/frontend/src/components/button.tsx

```tsx
// Example TypeScript code for Button component
import React from 'react';

type ButtonProps = {
  label: string;
};

const Button: React.FC<ButtonProps> = ({ label }) => {
  return <button>{label}</button>;
};

export default Button;


## MyProject/backend/api/postman.json

```json
{
  "info": {
    "name": "My API",
    "description": "API Documentation",
    "version": "1.0"
  },
  "item": [
    {
      "name": "GET /users",
      "request": {
        "method": "GET",
        "url": "/users"
      }
    }
  ]
}


## MyProject/backend/servers/server.py

```py
# Python code for server
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, world!"

if __name__ == "__main__":
    app.run(debug=True)


## MyProject/backend/servers/server-lite.py

```py
# Python code for lightweight server
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Lightweight Server Running!"

if __name__ == "__main__":
    app.run(debug=True, host='0.0.0.0', port=5001)

```
---

Feel free to modify this template and start sharing your projects using MinSSG!