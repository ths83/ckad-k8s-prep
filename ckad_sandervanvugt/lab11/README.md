Create a YAML file that runs a deployment with the name secretservice using the alpine image.
The deployment should use two variables, username which has set to "Anna" and password which has set to "secret". 
These variables must be added as a volume in the Pod and mounted in the directory etc users. Also ensure that the container in this Pod runs as user ID 1000.
