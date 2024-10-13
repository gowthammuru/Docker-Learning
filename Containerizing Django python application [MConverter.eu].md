**Containerizing Django python application:**

**1.**Copied the source codes, got to know the required dependencies to
run this application from requirements.txt.

2.Created a docker file to create a docker image with ubuntu as base
image and to install required dependencies like python, Django, tzdata.

![](media/image1.png){width="6.268055555555556in"
height="3.720833333333333in"}

Note: Got a error while trying to run the below docker file:

![](media/image2.png){width="6.268055555555556in"
height="3.609722222222222in"}

The error occurs because you\'re trying to install Python packages
globally in an environment that is externally managed, as mentioned by
the error message.

3\. Difference between Entry point and CMD:

Commands given in Entry point are unchangeable whereas we can change the
commands given in CMD

4.Creating a docker container with above source code and other
dependencies by executing "docker build -t
gowthamravic/django-python-app ."

![](media/image3.png){width="6.268055555555556in"
height="3.127083333333333in"}

6.Listing the available docker images by executing "docker images"
command:

![](media/image4.png){width="6.268055555555556in"
height="0.6243055555555556in"}

7.Executing the above created container and mapping the container's port
8000 with the host(192.168.29.47) port 8000 by executing command "docker
run -p 8000:8000 -it 'docker id':

![](media/image1.png){width="6.268055555555556in"
height="3.720833333333333in"}

8.Trying to access the web-application from browser:

![](media/image5.png){width="6.268055555555556in"
height="3.5229166666666667in"}

9.Pushing the docker container image to dockerhub repo by executing
command "docker push container name"

![](media/image6.png){width="6.268055555555556in"
height="1.4409722222222223in"}

10.Docker Hub:

![](media/image7.png){width="6.268055555555556in"
height="3.3944444444444444in"}

https://hub.docker.com/repository/docker/gowthamravic/django-phython-app/general
