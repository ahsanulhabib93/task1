*first we create image From /build directory using Dockerfile. docker build -t docker-username/repository-name:tag

From the deploy directory run the yaml file to deploy the application in kubernetes cluster and run the required sevice for the application kubectl apply -f <name-of-file>.yaml
Under src directory, all the required source code are available from where we can edit and push to the docker hub using Dockerfile and tag
