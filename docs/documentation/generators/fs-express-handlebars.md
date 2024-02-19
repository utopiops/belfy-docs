---
sidebar_position: 1
---

# fs-express-handlebars

The Full-Stack Node.js Express with Handlebars Views Generator (`fs-express-handlebars`) is an official generator in Belfy that enables developers to quickly scaffold full-stack CRUD applications using Node.js and Express framework with Handlebars views.

## Usage

To use the `fs-express-handlebars` generator, follow the steps below:

1. Ensure you have Belfy installed globally by running:
   ```bash
   npm install -g @belfy/cli
2. Create a folder for your project configuration and place your data definitions and customization files inside it.
3. Run the Belfy CLI with the create command, passing the path to your project configuration folder:
```bash
belfy create
```
4. Answer the prompts based on your preferences. The generator will use default configurations for now.
5. Once the generator completes, navigate to the generated project directory:
```bash
cd your-project-directory
```
6. Start the Docker containers for the database:
```bash
docker-compose up -d db    # Start the database container
```
7. After at least 30 seconds, start the application container:
```bash
docker-compose up -d app   # Start the application container
```
8. Access your application in your browser at http://localhost:3000.

