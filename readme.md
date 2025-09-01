
# LinkedIn Post Generator

This project is a simple Langchain Langgraph application designed to quickly generate multiple LinkedIn post drafts.

## Table of Contents

  - [Overview](https://www.google.com/search?q=%23overview)
  - [Features](https://www.google.com/search?q=%23features)
  - [Project Structure](https://www.google.com/search?q=%23project-structure)
  - [How to Run](https://www.google.com/search?q=%23how-to-run)
  - [License](https://www.google.com/search?q=%23license)
  - [To-do List](https://www.google.com/search?q=%23to-do-list)

## Overview

This application uses Langchain and Langgraph to create a tool for generating LinkedIn post drafts. The backend handles post generation and image creation using the Google Gemini API, while the frontend provides a user interface for inputting and managing the posts.

## Features

  - **Post Generation**: Generates multiple LinkedIn post drafts.
  - **Image Generation**: Creates images based on prompts using Google's Gemini API[cite: 178].
  - **Post Editing**: Allows editing posts with a Large Language Model (LLM)[cite: 181].
  - **Streaming Response**: The application is designed to stream responses as they are generated[cite: 179].
  - **Health Check**: The backend includes a health check endpoint at `/health` to ensure the service is running[cite: 178].

## Project Structure

The project is organized into `backend` and `frontend` services within a Docker container environment.

```
omarsahab-linkedin-post-generator/
├── readme.md
├── docker-compose.yml
├── LICENSE
├── backend/
│   ├── README.md
│   ├── Dockerfile
│   ├── main.py
│   ├── pyproject.toml
│   ├── requirements.txt
│   ├── vercel.json
│   ├── .dockerignore
│   ├── .python-version
│   └── app/
│       ├── agent.py
│       ├── img_gen.py
│       └── models.py
└── frontend/
    ├── README.md
    ├── Dockerfile
    ├── eslint.config.js
    ├── index.html
    ├── nginx.conf
    ├── package.json
    ├── tsconfig.app.json
    ├── tsconfig.json
    ├── tsconfig.node.json
    ├── vite.config.ts
    ├── .dockerignore
    └── src/
        ├── App.tsx
        ├── index.css
        ├── main.tsx
        ├── types.ts
        ├── vite-env.d.ts
        └── components/
            ├── ImageGenerator.tsx
            ├── Loader.tsx
            ├── PostCard.tsx
            └── PostInputForm.tsx
```

## How to Run

This project uses Docker Compose to manage both the backend and frontend services.

1.  **Configure Environment Variables**:
    Create a `.env` file in the root directory and add your Google API key.
    ```
    GOOGLE_API_KEY=your_google_api_key_here
    ```
2.  **Start the Services**:
    From the root directory, run the following command to build and start both the backend and frontend containers:
    ```sh
    docker-compose up --build
    ```
    [cite\_start]This command will build the `linkedin-post-gen-backend` and `linkedin-post-gen-frontend` images and run the services[cite: 159, 160, 161].

<!-- end list -->

  - The **backend** service will be available at `http://localhost:8000`[cite: 159].
  - The **frontend** service will be available at `http://localhost:3000`[cite: 161].

## License

This project is licensed under the **GNU General Public License, Version 3**. [cite\_start]You can find the full text of the license in the `LICENSE` file[cite: 161, 162].
