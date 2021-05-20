1. How long did it take to finish the test?
  In total 11-12 hours were spend on the test
2. If you had more time, how could you improve your solution?
  A better solution to expose our service to the public would be found and https would be implemented
3. What changes would you do to your solution to be deployed in a production environment?
  There would be different pods for the two containers in order to have different scaling settings
  and better observability. Also, kubeadm would be used instead of minikube as minikube is used to test things locally
  and it was a challenge to expose the service to external traffic. In addition, monitoring solutions would be deployed alongside our application.
4. Why did you choose this language over others?
  Flask apps are easy to write and Python is a language which is familiar to me
5. What was the most challenging part and why?
  The most challenging part was to expose the service to our external IP address. In the end, port forwarding was used as a workaround in order to expose the service.
