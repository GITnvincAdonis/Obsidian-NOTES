---
creation date: <% tp.file.creation_date() %>
---
[Aseprite](https://github.com/aseprite/aseprite) is the currently the go-to pixel art editing app. It is open source but compilations of the source code requires money to be accessed. The developers allow free use, as long you compile the app yourself.

> [!Example] [DOCKER CONTAINER FOR LINUX](https://github.com/nilsve/docker-aseprite-linux)
 
The setup steps provided for the repository is comprehensive but outdated.

> [!Danger] Required changes 
> ##### 1. Editing the Make file
> After cloning the repository, all "docker-compose" commands need to be update to "docker compose". docker-compose is a separate package but the command now comes with docker by default:
> ```
> IMAGE_NAME := docker-aseprite
> build: build-image
> docker run --rm \
> 	-v ${PWD}/output:/output \
> 	-v ${PWD}/dependencies:/dependencies \
> 	${IMAGE_NAME}
> build-compose:
> 	docker-compose build
> 	docker-compose up
> build-image:
> 	docker build -t ${IMAGE_NAME} .
> ```
> ## TO
> ```
> IMAGE_NAME := docker-aseprite
> build: build-image
> docker run --rm \
> 	-v ${PWD}/output:/output \
> 	-v ${PWD}/dependencies:/dependencies \
> 	${IMAGE_NAME}
> build-compose:
> 	docker compose build
> 	docker compose up
> build-image:
> 	docker build -t ${IMAGE_NAME} .
> ```
> ##### 2. In the compile.sh file, add the following after "export PATH="${PWD}/depot_tools:${PATH}"" (line 17):
> ```
> gclient
> ```
> 


After the modifications, run:
```
make build-compose
```

Reference documentation for launch instructions

> [!Bug] Debugging Claude conversation 
> https://claude.ai/chat/653c9e0e-60f5-4672-9cfb-16b185095b9e

Path of build:
```
Documents/docker-aseprite-linux/output/aseprite/build/bin
```

Link to original: [[2025-05-31]]