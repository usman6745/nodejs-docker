# nodejs-docker
Deploying nodejs project on docker and running the container

-> Install nodejs app on ubuntu server with deps
-> configure nodejs -> and run on port 3000  -> it will be work fine -> curl http://<ip-addr>:3000
-> Install docker on ubuntu - ce edition
-> create a docker file for nodejs application on the name of Dockerfile
  
-> Created a docker image out of Dockerfile

# sudo docker build -t Dockerfile .
-> Run a container out of existed docker image on the port 90  -> 90:8080 (implies)

# sudo docker run --name nodejs1 -p 90:8080 -d <dockerhub-username>/<dockerimage-name>

-> check the container is working fine or not

# sudo docker ps 

-> go to browser and checkc the url -> http://<ip-addr>:90

-> check the all existed containers -> 
# sudo docker ps -a

-> Now stop the container and remove the existed containers (docker rmi <container-id>)
# sudo docker rmi <container-id>
 
-> -> Log into docker hub

# sudo docker login -u <dockerhub-username> -p <dockerhub-passwd>

-> push the existed docker image into my own docker hub repo - public

# sudo docker push <image-name>
  
-> here in ubuntu -> remove the existed docker images 

# sudo docker ps
# sudo docker ps -a 
# sudo docker images -a
# sudo docker system prune -a
# sudo docker images 

-> Now pull the image from my own dockerhub (nodejs)

# sudo docker pull <dockerhub-username>/<docker-imagename>
  
-> create a container out of it and ran on port 90

# sudo docker run --name nodejs1 -p 90:8080 <docker-image-name>
  
  # sudo docker logs <docker-container-name/id>
  # sudo docker inspect <docker-container-name/id>
  
 # sudo docker ps 
 =----------------------------------=
Resource:  
https://www.digitalocean.com/community/tutorials/how-to-build-a-node-js-application-with-docker
