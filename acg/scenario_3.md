# Scenario

_From: https://learn.acloud.guru/handson/53df2b3e-6346-4dd3-997a-3db86593334c/course/d068441f-75b4-4fe8-a7a6-df9153f24a35_

Our company has a Kubernetes cluster that is running several pods and services. A service called oauth-provider in the gem namespace has stopped working. Our task is to investigate the service and determine what is causing the problem, save some relevant data for future analysis, and then fix the problem.

The broken service is oauth-provider. It is located in the gem namespace.
- Identify which Kubernetes object is broken and causing the service to fail. 
- Save the name of the object in the file /usr/ckad/broken-object-name.txt.
- Save the object's summary data in JSON format to the file /usr/ckad/broken-object.json.
- Edit the object to fix the problem.
- The oauth-provider service is a NodePort service listening on port 30080, so we can test it using curl localhost:30080.
- Note that there may be other objects in the cluster which appear to be broken. Our task is to identify what specifically is causing the oauth-provider service to fail. Ignore any object which doesn't affect the oauth-provider service.