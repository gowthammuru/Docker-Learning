1.Login in to Dockerhub:

![](media/image1.png){width="6.268055555555556in" height="1.1625in"}

Docker hub is a repository to save Docker images.

2.First Docker File:

![](media/image2.png){width="6.268055555555556in" height="3.71875in"}

The above docker file will help to create a container with ubuntu as
base image, /app as working directory and install python in that image.

3.Creating a docker image by executing command "docker build -t
gowthamravic/my-first-docker-file ." (-t means TAG)

![](media/image3.png){width="6.268055555555556in"
height="3.2402777777777776in"}

4.Listing available docker images by executing command "docker images"

![](media/image4.png){width="6.268055555555556in"
height="0.9722222222222222in"}

5.Running the above created docker container by executing command
"docker run gowthamravic/my-first-docker-image"

![](media/image5.png){width="6.268055555555556in"
height="0.7486111111111111in"}

6.Pushing the above created container image to dockerhub repo by
executing command "docker push gowthamravic/my-first-docker-image"

![](media/image6.png){width="6.268055555555556in"
height="1.198611111111111in"}

7.Docker hub Repo:

![](media/image7.png){width="6.268055555555556in"
height="3.388888888888889in"}

Link:
https://hub.docker.com/repository/docker/gowthamravic/my-first-docker-image/general
