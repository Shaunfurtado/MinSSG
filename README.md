# MinSSG

MinSSG is an online static code-sharing platform that allows users to showcase project structures directly from a markdown file. With this tool, you can present your project’s folder structure, code snippets, and individual files in an interactive, static format.

[Live Link Demo](https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=https://gist.githubusercontent.com/Shaunfurtado/2036bc36cf9d86fdbf680a69ae3f8d8d/raw/95f671db6442df4a5663ad2e06f4738c2baa2369/ConRAG.md)

## Features
- Display project structure with tree view.
- Render code files from markdown with appropriate syntax highlighting.
- Easy-to-use markdown template to get started.

## Usage Instructions for MinSSG

To use MinSSG for displaying your project structure and code, follow these steps:

1. **Prepare Your Markdown File:**
    - Create a markdown file with your project structure and code snippets. You can use the [example template](#writing-the-markdown) for guidance.
   
2. **Host Your Markdown File:**
    - Upload your markdown file to a pastebin or gist service that provides a raw URL. Here are some options:
        - **[GitHub Gist](https://gist.github.com/)**: Create a gist with your markdown content and copy the raw URL.
        - **[Rentry.co](https://rentry.co/)**: Paste your markdown into Rentry.co and get the raw URL.
        - Any other pastebin-like service that allows fetching a raw URL of your content.
   
3. **Use MinSSG to Display Your Project:**
    - Visit the MinSSG viewer at:  
      [MinSSG Viewer](https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=<your-raw-url-here>)
      ```url
      https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=<your-raw-url-here>
      ```

    - Replace `<your-raw-url-here>` with the raw URL of your markdown file. For example, if you’re using the Gist link, it would look like this:
      ```url
      https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=https://gist.githubusercontent.com/Shaunfurtado/2036bc36cf9d86fdbf680a69ae3f8d8d/raw/95f671db6442df4a5663ad2e06f4738c2baa2369/ConRAG.md
      ```

		[Live Link Demo](https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=https://gist.githubusercontent.com/Shaunfurtado/2036bc36cf9d86fdbf680a69ae3f8d8d/raw/95f671db6442df4a5663ad2e06f4738c2baa2369/ConRAG.md)

4. **View Your Project Structure:**
    - Once you paste the URL in your browser and load the page, MinSSG will display your project structure and code files as defined in your markdown.

---

### Example URL Usage

Here’s an example of a complete URL to use in your browser to load a markdown file:

```url
https://shaunfurtado.is-a.dev/MinSSG/?fileUrl=https://gist.githubusercontent.com/Shaunfurtado/2036bc36cf9d86fdbf680a69ae3f8d8d/raw/95f671db6442df4a5663ad2e06f4738c2baa2369/ConRAG.md
```

This will load the markdown file from the provided Gist URL and display it using MinSSG.

---

### Notes:
- Make sure the URL you use is the **raw** version of the file. If you're using Gist, click on the “Raw” button to get the correct URL.
- The URL parameter `fileUrl` must point to the raw content of your markdown file.


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