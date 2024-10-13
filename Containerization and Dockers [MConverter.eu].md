**Containerization and Dockers**

**1.What is containerization?**

Containerization is a lightweight form of virtualization that involves
packaging an application and its dependencies into a single unit called
a container. Unlike traditional virtualization, which requires an entire
operating system for each instance, containers share the host OS kernel
while running isolated processes. This allows for:

- **Portability**: Containers can run consistently across different
  environments, whether on a developer\'s laptop, a testing server, or a
  production cloud platform.

- **Scalability**: Applications can be easily scaled by creating
  multiple container instances to handle increased load.

- **Efficiency**: Containers use fewer resources than virtual machines,
  allowing for quicker startup times and better utilization of system
  resources.

- **Simplified Deployment**: With everything bundled together, deploying
  applications becomes faster and more predictable.

**2.What is docker?**

Containerization is the technology, and Docker is platform which
implements containerization.

**3.Docker installation in ubuntu VM:**

root@Ubunutu:/home/vboxuser/Desktop/Devops/Docker-Zero-to-Hero# history

1 apt-get install ca-certificates curl

2 install -m 0755 -d /etc/apt/keyrings

3 curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o
/etc/apt/keyrings/docker.asc

4 chmod a+r /etc/apt/keyrings/docker.asc

5 echo \"deb \[arch=\$(dpkg \--print-architecture)
signed-by=/etc/apt/keyrings/docker.asc\]
https://download.docker.com/linux/ubuntu \\

6 \$(. /etc/os-release && echo \"\$VERSION_CODENAME\") stable\" \| sudo
tee /etc/apt/sources.list.d/docker.list \> /dev/null

7 sudo apt-get update

8 sudo apt-get install docker-ce docker-ce-cli containerd.io
docker-buildx-plugin docker-compose-plugin

9 sudo docker run hello-world

10 uname -m

11 curl -LO
<https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64>

**4.Docker installation verification:**

Execute docker run hello-world:

![](media/image1.png){width="6.785755686789152in"
height="2.834286964129484in"}

**5.Difference between Virtualization and Containerization:**

\*For virtualization we need hypervisors like virtual box or vmware
where as for containerization no hypervisors are required.

\*In virtualization, there will be a guest operating system, but where
as in containers, it will not have complete OS, it will only have
application dependencies.

\*Container are light weight than VM.
