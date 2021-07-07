# Lesson 7 Lab

## Target
Create a YAML file that starts a Deployment for Nginx and introduce image version 1.9 and start five replicas. The Deployment should have the label app is proxy and also configure the Deployment such that when it is upgraded, no more than two pods will be unavailable at the same time.

### Useful commands 

- View generated deployment yaml but no creation, save to new yaml file: 
kubectl create deployment nginx-lab7 --image=nginx:1.9 --replicas=5 -o=yaml --dry-run > lab7.yaml

- Change maxUnavailable to 2 instead of 25%.

- Create deployment :
kubectl create -f lab7.yaml
