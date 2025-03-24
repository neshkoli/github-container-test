# Hello World Docker Project

This project demonstrates a simple "Hello, World!" application using Node.js, packaged in a Docker container. It also includes a GitHub Actions workflow to automate the building and publishing of the Docker image to the GitHub Container Registry.

## Project Structure

```
hello-world-docker
├── .github
│   └── workflows
│       └── docker-publish.yml
├── Dockerfile
├── app.js
├── package.json
└── README.md
```

## Getting Started

To build and run the Docker container, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/hello-world-docker.git
   cd hello-world-docker
   ```

2. **Build the Docker image:**

   ```bash
   docker build -t hello-world-docker .
   ```

3. **Run the Docker container:**

   ```bash
   docker run -p 3000:3000 hello-world-docker
   ```

4. **Access the application:**

   Open your browser and go to `http://localhost:3000`. You should see "Hello, World!" displayed.

## GitHub Actions Workflow

This project includes a GitHub Actions workflow defined in `.github/workflows/docker-publish.yml`. This workflow will automatically build and publish the Docker image to the GitHub Container Registry whenever changes are pushed to the main branch.

### How to Use the Workflow

1. Ensure you have set up the GitHub Container Registry in your repository settings.
2. Push your changes to the main branch.
3. The workflow will trigger automatically, building the Docker image and pushing it to the registry.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.