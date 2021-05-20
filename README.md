For our application, we will need to have installed:
1. [Docker](https://docs.docker.com/engine/install/ubuntu/)
2. [Kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
3. [Minikube](https://minikube.sigs.k8s.io/docs/start/)
4. [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

(In case you encounter a "permission denied" error while starting Docker, you can use [this](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue) solution)

Instructions to run the app:

1. Port 80 must be exposed on our machine (and 443 for https traffic).
2. Clone the repository by running the command "git clone https://github.com/siamsot/nginx-rproxy-k8s"
2. Start Minikube with "minikube start --extra-config=apiserver.service-node-port-range=1-65535"
   This is done because we've set the nodePort to 80 which isn't in the default range
3. Navigate to the directory where our configuration yaml file is with "cd nginx-rproxy-k8s"
4. Edit the config.yaml file and change the {ip or domain} field to your machine's IP address
5. Deploy our application with "kubectl apply -f config.yaml"
6. Run the command "sudo kubectl --address 0.0.0.0 port-forward svc/hello-service 80:80"
   It's needed to run the command with sudo privileges in order to expose the service to port 80

   
This solution was chosen over a solution with docker compose as it is closer to a production environment
