# AT2024 Converter and Recognizer Service 

# Description
This repository contains two Dockerized services:
1. **AT2024Progra2ConverterService**: A Flask-based converter service.
2. **AT2024Progra2MLService**: A machine learning service for object, gender and face recognition.
Both services use Docker and are orchestrated via Docker Compose, with PostgreSQL as the database.

# 📂 Project Structure
Within the repository you can find two folders, each one containing a docker-compose file. Both files can build and run the Docker container with the services, however, one of them needs the services repositories to be cloned in your local machine. The other one uses the Github repository addresses, so there is no need to clone the repositories locally.

```
├── DockerWithGithub/          
│   ├── .env
│   └── docker-compose.yml
│   
├── DockerWithLocal/           
│   ├── AT2024Progra2ConverterService/      # You need to close this repository
│   │    └── [corresponding files...]
│   │
│   ├── AT2024Progra2MLService/             # You need to close this repository
│   │    └── [corresponding files...]
│   │
│   ├── .env
│   └── docker-compose.yml
│
└── README.md               # Repository documentation
```
# Installation and how to run Docker

## Running Docker using Github repositories
In this case there is no need to clone the repos locally. Create the .env file and run the following command. Also make sure that Docker Desktop is running.
```bash
   docker compose up --build -d
```

## Running Docker using Cloned repositories into local machine
Within the DockerWithLocal folder, you need to clone the repositories for the converter and ML services.

Using the following commands:
```bash
   git clone https://github.com/jpsandovaln/AT2024Progra2ConverterService.git
   git clone https://github.com/jpsandovaln/AT2024Progra2MLService.git
   ```

After cloning the repositories and pulling the last changes from the desired branch, you can run docker with the following command:
```bash
   docker compose up --build -d
```


