1.What is bind mount?
we can bind a directory in a host machine to a directory in a container, containers can use this directory to store logs, place outputs etc.

2.What is volumes?
Volumes is the logical partition created in host machine which can also be used by container to store, save, place various information.

3.Creating a volume named "test" using the command " docker volume create test" and verifying whether a volume got crated or not by using command "docker volume ls":
![image](https://github.com/user-attachments/assets/192b9b92-1e21-40b3-8748-71eb7821fce9)

4.Mounting the above crated volume to a container using command "docker run -d --mount source=test,target=/app docker iamge id"
![image](https://github.com/user-attachments/assets/28465055-d692-4e50-8a62-fc8618c81a32)

Mounted a newly created voulme to the container image.
