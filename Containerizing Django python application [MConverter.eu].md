**Containerizing Django python application:**

**1.**Copied the source codes, got to know the required dependencies to
run this application from requirements.txt.

2.Created a docker file to create a docker image with ubuntu as base
image and to install required dependencies like python, Django, tzdata.

![docker new file](https://github.com/user-attachments/assets/dccc06c4-f6a7-4bfb-9898-680e86a46076)


Note: Got a error while trying to run the below docker file:
![Docker file](https://github.com/user-attachments/assets/eecc9f79-519b-46d0-acdd-6f29a9652c5e)

The error occurs because you're trying to install Python packages
globally in an environment that is externally managed, as mentioned by
the error message.

3. Difference between Entry point and CMD:

Commands given in Entry point are unchangeable whereas we can change the
commands given in CMD

4.Creating a docker container with above source code and other
dependencies by executing "docker build -t
gowthamravic/django-python-app ."

![docker build new](https://github.com/user-attachments/assets/d7cefe89-e4c8-4d37-bfef-95ba25f731f0)


6.Listing the available docker images by executing "docker images"
command:

![docker images](https://github.com/user-attachments/assets/f6704628-86df-43e4-89ce-a22d1c8105ea)

7.Executing the above created container and mapping the container's port
8000 with the host(192.168.29.47) port 8000 by executing command "docker
run -p 8000:8000 -it 'docker id':

![docker run](https://github.com/user-attachments/assets/648c42f9-987f-40f3-90d4-c98bf8016502)


8.Trying to access the web-application from browser:
![result](https://github.com/user-attachments/assets/1e14d0da-8cba-4ff8-8555-470d0aad744c)



9.Pushing the docker container image to dockerhub repo by executing
command "docker push container name"

![docker push](https://github.com/user-attachments/assets/e686e3de-96e7-42fb-90f9-18219d7710b4)


10.Docker Hub:

![docker hub](https://github.com/user-attachments/assets/e79a1250-acac-4461-924d-b34ad141cd80)


https://hub.docker.com/repository/docker/gowthamravic/django-phython-app/general

11.Downloading the django container in another host machine by executing command "docker pull container-name" command:
![image](https://github.com/user-attachments/assets/24e2ec3b-0c59-4598-a47d-339ba520e60a)

12.Starting the container and port mapping with host using command "docker run -p 8000:8000 -it docker-id: command:
![image](https://github.com/user-attachments/assets/751d8fb3-2f22-48e1-9b58-9fdf64d2d0f7)

13.Result:
![image](https://github.com/user-attachments/assets/b11a07e8-7f28-45e5-810d-a023fcde0bec)


