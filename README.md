# JOB-INTERVIEW-CHATBOT

Semester 1 project for the Module "Knowledge Representation and Natural Language Processing" by Elena Kuss for the Reutlingen University Business Informatics Master of Science. This repository contains the complete code of the bot.

## Setup

### Clone the repository

To get started, first clone the repositories with all of its submodules.

Cloning with one command:

```bash
git clone --recursive https://github.com/NicoDoebele/job-interview-chatbot.git
```

_Alternatively_, clone with a seperate submodule pull:

```bash
git clone https://github.com/NicoDoebele/job-interview-chatbot.git
git submodule init && git submodule update
```

### Start the project

In order to easily deploy the project docker needs to be installed.

To start the project, simply run the deploy.sh script:

```bash
sh deploy.sh
```

_Alternatively_, you can run the commands yourself:

```bash
docker compose up -d
# This part requires ollama to be up and running in docker
docker exec -it job-interview-chatbot-ollama ollama pull llama3.2
```

#### Starting the project without docker

In case you do not wish to use docker, you will need to set up the projects seperately. No guide will be provided for this process. Each project has a requirements.txt file to set up your virtual environments. Both projects were created on MacOS with an arm chip using pyton version 3.9.21.

For the application to be fully functional Ollama needs to be accessible with llama3.2:latest running. The chatbot needs to be running with rasa actions enabled. The frontend can also optionally be started and used. The docker compose file and dockerfiles can be used for refference when setting up the project locally.
