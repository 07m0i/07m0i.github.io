# 07m0i.github.io
<!DOCTYPE html>
<html>
<head>
    <title>README Generator</title>
    <style>
        body { font-family: Arial, sans-serif; max-width: 800px; margin: 0 auto; padding: 20px; }
        textarea { width: 100%; height: 300px; margin: 10px 0; }
        button { background: #2ea44f; color: white; border: none; padding: 10px 15px; cursor: pointer; }
        button:hover { background: #22863a; }
    </style>
</head>
<body>
    <h1>README Generator</h1>
    
    <div>
        <label>Project Title:</label>
        <input type="text" id="title" placeholder="My Awesome Project">
    </div>
    
    <div>
        <label>Description:</label>
        <textarea id="description" placeholder="A brief description of your project..."></textarea>
    </div>
    
    <button onclick="generateReadme()">Generate README</button>
    
    <h3>Preview:</h3>
    <textarea id="output" readonly></textarea>
    
    <script>
        function generateReadme() {
            const title = document.getElementById('title').value || 'My Project';
            const description = document.getElementById('description').value || 'A GitHub project';
            
            const readme = `# ${title}

## Description
${description}

## Features
- Feature 1
- Feature 2

## Installation
\`\`\`bash
git clone https://github.com/yourusername/reponame.git
\`\`\`

## Usage
How to use your project...

## License
[MIT](https://choosealicense.com/licenses/mit/)`;
            
            document.getElementById('output').value = readme;
        }
    </script>
</body>
</html>
