Tutorial: Create a Docker image for a Go application

To build docker image :- 
`docker build -t docker-go-app -f Dockerfile .`

To Run the app :- 
`docker run -d -p 8080:8080 docker-go-app`

To build the docker image with mounted volume :-
`docker build -t go-docker-volume -f Dockerfile.volume .`
`docker run -d -p 8080:8080 -v /Users/sumisaha/go/src/github.com/saha/docker-go-app/logs:/app/logs go-docker-volume`

To build the optimized docker image with mounted volume :-
`docker build -t go-docker-optimized -f Dockerfile.multistage .`

Took help from https://www.callicoder.com/docker-golang-image-container-example/ to create this project

Create a `logs` folder in the current repo before running the container, then use
`docker run -d -p 8080:8080 -v /Users/sumisaha/go/src/github.com/saha/docker-go-app/logs:/app/logs go-docker-optimized`
