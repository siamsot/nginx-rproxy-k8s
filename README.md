For our application, we will need to have installed:
1. [Docker](https://docs.docker.com/engine/install/ubuntu/)
2. [Kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
3. [Minikube](https://minikube.sigs.k8s.io/docs/start/)

(In case you encounter a "permission denied" error while starting Docker, you can use [this](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue) solution)

Instructions to run the app:

1. Port 80 must be exposed on our machine (and 443 for https traffic).
2. Clone the repository by running the command "git clone https://github.com/siamsot/nginx-rproxy-k8s"
2. Start Minikube with "minikube start --extra-config=apiserver.service-node-port-range=1-65535"
   This is done because we've set the nodePort to 80 which isn't in the default range
3. Navigate to the directory where our configuration yaml file is with "cd nginx-rproxy-k8s"
4. Deploy our application with "kubectl apply -f config.yaml"

This solution was chosen over a solution with docker compose as it is closer to a production environment
