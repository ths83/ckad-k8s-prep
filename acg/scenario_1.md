# Scenario

_From: https://learn.acloud.guru/handson/befc5a89-3288-412a-b6ae-68925d5f967b/course/d068441f-75b4-4fe8-a7a6-df9153f24a35_

Our pizza restaurant is working on a new web application designed to run in a Kubernetes cluster. The development team has designed a web service which serves a list of pizza toppings. The team has provided a set of specifications which the pizza topping web service needs in order to run.

We have been asked to create a deployment that meets the app's specifications. Then, we need to expose the application using a NodePort service. This setup should meet the following criteria:

- All objects should be in the pizza namespace. This namespace already exists in the cluster.
- The deployment should be named pizza-deployment.
- The deployment should have 3 replicas.
- The deployment's pods should have one container using the linuxacademycontent/pizza-service image with the tag 1.14.6.
- Run the container with the command nginx.
- Run the container with the arguments "-g", "daemon off;".
- The pods should expose port 80 to the cluster.
- The pods should be configured to periodically check the /healthz endpoint on port 8081, and restart automatically if the request fails.
- The pods should not receive traffic from the service until the / endpoint on port 80 responds successfully.
- The service should be named pizza-service.
- The service should forward traffic to port 80 on the pods.
- The service should be exposed externally by listening on port 30080 on each node.