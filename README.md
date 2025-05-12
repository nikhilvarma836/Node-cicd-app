# 🚀 Node.js CI/CD Pipeline with GitHub Actions & Docker

This project demonstrates how to automate the build and deployment of a sample Node.js web app using a CI/CD pipeline configured with **GitHub Actions** and **DockerHub**.

---

## 📁 Project Structure

nodejs-demo-app/
├── .github/
│ └── workflows/
│ └── main.yml # CI/CD workflow definition
├── app.js # Sample Node.js app
├── app.test.js # Optional test file
├── Dockerfile # Docker image instructions
├── package.json
└── README.md


---

## 🎯 Objective

Automate the build, test, and deployment process for a Node.js app using GitHub Actions. The pipeline should:

- Trigger on push to `main`
- Install dependencies & run tests
- Build a Docker image
- Push the image to DockerHub

---

## 🛠 Tools & Technologies

- **GitHub**
- **GitHub Actions**
- **Node.js**
- **Docker**
- **DockerHub**

---

## 🧪 Sample Node.js App

Here’s a minimal example (`app.js`):

```js
const http = require('http');
const port = 3000;
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, CI/CD!\n');
});
server.listen(port, () => {
  console.log(`Server running on port ${port}`);
});

