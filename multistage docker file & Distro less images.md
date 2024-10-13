1.What is Multistage Docker file?
Answer: In order to reduce the size of docker images drastically, first we will create a build using a base image,source code and other required dependancies to generate a binary file of the application, then we will copy that binary file in to a new minimal base image such as "scratch".
Ex:
*Using ubuntu as base image, copied source code and installed other dependancies and created the binary file of the application and created a build using this.
*Copied the above binary file in to a new base image named "Scratch"

Multi statge docker file not only reduces size of the image, but it also helps running the containers securely, since it will not have any other OS-related stuffs.

2. What is distro-less images?
    Distroless images are Docker images that contain only the essential application and its runtime dependencies, without including an entire operating system distribution like Ubuntu, CentOS. The goal 
 is to create lightweight, secure, and minimal container images, reducing attack surface and improving performance.

3. Creating a container image for a "go" language calculator app without multi-stage docker file:
   ![image](https://github.com/user-attachments/assets/54d2f653-18d6-485c-9505-24e7a481048d)

4.Creating a build by executing command "docker build -t gowthamravic/go-lang-app-without-multistage ." (Without multi-stage docker file)
![image](https://github.com/user-attachments/assets/7737987f-872d-4387-ba35-75be2e5a4d56)

5.Seeing the size of the docker container that was created using non multi stage docker file:
![image](https://github.com/user-attachments/assets/0313821f-af80-4c7e-8e6a-7a9a1ff3c0e0)
Image size is around 651MB

6. Creating a build with multi stage docker file:
   ![image](https://github.com/user-attachments/assets/c0e47fa7-ac40-46c0-a203-a138a4537d85)

 ![image](https://github.com/user-attachments/assets/ee21cf4e-5e4f-423e-bd6c-8b7f090ed256)

7.Verifying the size of image created using multi-stage docker file:
![image](https://github.com/user-attachments/assets/253b2fde-7ec8-4d3a-b2f2-1f0be6a62252)


Size of this image is around 1.96 MB.

**Thus by using multi-stage docker file we have reduced the size of the image barely from 650 mb to 1.96 mb!
**

