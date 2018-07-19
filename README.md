# learn-kubernetes
have a taste of kubernetes
<br/>
create minikube cluster<br/>
minikube start --vm-driver=hyperkit<br/>
open dashboard<br/>
minikube dashboard<br/>
<br/><br/>
create a node js hello world<br/>
<br/><br/>
create a docker image<br/>
Because this tutorial uses Minikube, instead of pushing your Docker image to a registry, you can simply build the image using the same Docker host as the Minikube VM, so that the images are automatically present. To do so, make sure you are using the Minikube Docker daemon:<br/>
run this:<br/>
eval $(minikube docker-env)<br/>
Note: Later, when you no longer wish to use the Minikube host, you can undo this change by running eval $(minikube docker-env -u).<br/>
<br/><br/>
build the image<br/>
docker build -t hello-node:v1 .	<br/>
<br/><br/>
Create a Deployment<br/>
kubectl run hello-node --image=hello-node:v1 --port=8080 --image-pull-policy=Never<br/>
view deployment<br/>
kubectl get deployments<br/>






