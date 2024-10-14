Docker offers three different types of networks, such as:
*Bridge network: Bridges the container and host machine with the help of bridge network, the default bridge network is veth0(docker0).In this type of network host and container will be in different subnet
*Host network: in this type of network, both host and container will be in same subnet.
*Overlay network: Networking between the containers in different nodes.

![image](https://github.com/user-attachments/assets/cbfe281e-6159-488b-9ce7-03a5e2875e90)

Example:
Requirement: 1.Create three containers and put two containers in default bridge network and the third one in custom created bridge network. So that container 3 is isolated from container 1 & 2
             2.Crate a container and map it to host network(Same network as host).


Solution:
Requirement 1:
*Created two containers named "login"(IP:172.17.0.2) and logout"(IP:172.17.0.3)":
![image](https://github.com/user-attachments/assets/3a8b0783-3b23-4188-80be-192611e4be65)

*Output of docker inspect login and docker inspect logout commands:
![image](https://github.com/user-attachments/assets/cb3b36b9-9c69-4cce-ad19-1c4441c84eb7)

![image](https://github.com/user-attachments/assets/42bca957-d99f-4f69-b8c3-eaaab0d884de)

*Pinging from C1 to C2:
![image](https://github.com/user-attachments/assets/34c508a0-93c7-45ec-b7c9-8a2ef18a4271)

*Creating a new custom bridge network named "testsubnet" by executing command "docker network create testsubnet":
![image](https://github.com/user-attachments/assets/3819720d-2bdd-4c87-9d75-7daa7b701eda)

*Creating third container named "finance" and mapping it to above crated custom bridge network named "testsubnet" by executing commmand " docker run -d --network=testsubnet --name finance nginx:latest"
![image](https://github.com/user-attachments/assets/4a5ee41d-4941-41d9-97b5-d9ee0e8b2146)

![image](https://github.com/user-attachments/assets/ad2f48c3-9ad9-477c-a23b-c64596e21e38)

![image](https://github.com/user-attachments/assets/7a362af5-1f92-46e3-a066-8002f0a89ad3)

The third container is mapped to a subnet 172.18.0.0/24(testsubnet) whereas container 1 & 2 are mapped to subnet 172.17.0.0/24(docker0).

*Trying to ping c3 from c1:
![image](https://github.com/user-attachments/assets/676d78d2-c760-4f5f-8b3c-472d33439365)

Unable to ping, thus C3 is isolated from C1 and C2, thus we acheieved requirement 1.

Requirement 2:
*Creating a new container and mapping it to existing host network:
![image](https://github.com/user-attachments/assets/a0ffc0d6-a656-40d8-b906-e61ba872bf44)
![image](https://github.com/user-attachments/assets/4719659b-256c-4721-bb44-db81326753c0)

![image](https://github.com/user-attachments/assets/67bf9bb2-8504-4fcf-8879-7299e0186bf5)



Thus we acheived Requirement 2 also.





