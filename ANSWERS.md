1. How long did it take to finish the test?
  In total 7-8 hours were spend on the test
2. If you had more time, how could you improve your solution?
  A better solution to expose our service to the public would be found and https would be implemented
3. What changes would you do to your solution to be deployed in a production environment?
  There would be different pods for the two containers in order to have different scaling settings
  and better observability. Also, a public cloud load balancer would be used to expose the service or an
  external name and a config map would be used for the nginx configuration.
4. Why did you choose this language over others?
  Flask apps are easy to write and Python is a language which is familiar to me
5. What was the most challenging part and why?
  The most challenging part was to expose the service with an external IP address which wasn't achieved in the end.
  I tried various solutions, with LoadBalancer with minikube tunnel instead of NodePort without success. However, the solution was working locally.
