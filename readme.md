To build docker image :- 
`docker build -t docker-go-app .`

To Run the app :- 
`docker run -d -p 8080:8080 docker-go-app`

To build the docker image with mounted volume :-
`docker build -t go-docker-volume -f Dockerfile.volume .`

To build the optimized docker image with mounted volume :-
`docker build -t go-docker-optimized:0.1 -f Dockerfile.multistage .`

Took help from https://www.callicoder.com/docker-golang-image-container-example/ to create this project

Create a `logs` folder in the current repo before running the container, then use
`docker run -d -p 8080:8080 -v /Users/sumisaha/go/src/github.com/saha/docker-go-app/logs:/app/logs go-docker-optimized`
