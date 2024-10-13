1.Login in to Dockerhub:

![dockerhub login](https://github.com/user-attachments/assets/a2347750-af25-41c4-ba03-0c65c8b8f36c)


Docker hub is a repository to save Docker images.

Note: Copied the source code(it's a python application to print "HelLo world") from Abishek verammalla git hub page:
https://github.com/iam-veeramalla/Docker-Zero-to-Hero/tree/main/examples/first-docker-file

2.First Docker File:

![Docker file](https://github.com/user-attachments/assets/a9c6157e-437c-4b4b-8c50-9ec5accd8699)


The above docker file will help to create a container with ubuntu as
base image, /app as working directory and install python in that image.

3.Creating a docker image by executing command "docker build -t
gowthamravic/my-first-docker-file ." (-t means TAG)

![docker build](https://github.com/user-attachments/assets/c7149f52-95e5-4372-a20a-f48cd637d0ea)


4.Listing available docker images by executing command "docker images"

![image](https://github.com/user-attachments/assets/00f59d71-31ee-4ecd-bbf9-0b25d92a40ec)


5.Running the above created docker container by executing command
"docker run gowthamravic/my-first-docker-image"

![docker build](https://github.com/user-attachments/assets/b55b5971-0fe1-4e24-a71f-fdd3ebf43a40)


6.Pushing the above created container image to dockerhub repo by
executing command "docker push gowthamravic/my-first-docker-image"

![docker push](https://github.com/user-attachments/assets/9289a11a-9e27-4a20-b3f9-4481ee46b8d9)


7.Docker hub Repo:

![dockerhub](https://github.com/user-attachments/assets/4362eca7-9e68-450e-b30f-151550fb304d)


Link:
https://hub.docker.com/repository/docker/gowthamravic/my-first-docker-image/general
