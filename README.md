# https://www.jenkins.io/doc/book/installing/docker/



"# install-jenkins-docker" 



# Create a bridge network in Docker using the following docker network create command:



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/b1ee2165-23e8-4951-a2db-f95473f06088)




# In order to execute Docker commands inside Jenkins nodes, download and run the docker:dind Docker image using the following docker run command:

![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/ce1e8ebe-679d-4d82-9416-a8c763d0acf8)





# Create a Dockerfile with the following content:
![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/a4f4edc2-d040-4295-8f29-1c3686069c15)





# Build a new docker image from this Dockerfile, and assign the image a meaningful name, such as "myjenkins-blueocean:2.414.2-1":



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/31f6ebfe-40ba-4a67-af15-515e1ccf7aef)





# Run your own myjenkins-blueocean:2.414.2-1 image as a container in Docker using the following docker run command:


![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/5b599d28-6b9a-4f12-b241-fdba289277be)





# Proceed to the Post-installation setup wizard.
# https://www.jenkins.io/doc/book/installing/docker/#setup-wizard



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/2aa6c9a7-a099-47de-81d3-c262fbc797f3)



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/ecf8abf7-7ebd-4aca-aed5-15fa58ecaa82)




![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/e349a3e1-bf8d-4a42-b34d-ba2a7743d2b0)



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/ca3b75e4-9d59-4844-8475-d1fe97a7f58e)

![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/8713286e-feb6-44fa-a16a-c4b52f372814)


![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/2caa691d-389c-4723-8001-edd30cdf1875)


# Create First Admin User

![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/9dd3e882-eb18-4d26-9946-984f6dc7c78a)



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/b052e268-06e5-42a0-9d37-3c7d34861adf)







![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/47ff4187-4081-499a-ad60-295ea7b5a3dc)


![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/ca983627-b707-42e9-abe1-22ef08c12b5a)






![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/a666907e-70c0-4789-9062-d42e988dfeac)





# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash
# docker exec -it — user=root <Container_Name or Container_Id> /bin/bash


# apt-get update
# apt-get install vim
# /var/jenkins_home
# vi config.xml

#  vi docker-compose.yml  
  version: '3'
  services:
    jenkins:
      container_name: 'jenkins'
      image: 'jenkins/jenkins:latest'
      restart: always
      ports:
        - 19800:8080
        - 19801:50000
      volumes:
        - ./jenkins:/var/jenkins_home
      environment:
        TZ: "Asiz/Seoul"


 # service --status-all
 # 
 #  docker pull jenkins/jenkins:lts
 # $ sudo docker run -d -p 8080:8080 -v /jenkins:/var/jenkins_home --name jenkins -u root jenkins/jenkins:lts
 # sudo docker-compose up -d
      
      version: "3"
      services:
        jenkins:
          image: jenkins/jenkins:lts
          user: root
          volumes:
            - ./jenkins:/var/jenkins_home
          ports:
            - 8080:8080  




 
 #  Jenkins 관리 > Script Console 에서 위의 스크립트를 입력하여 타임존을 서울로 설정
   System.setProperty('org.apache.commons.jelly.tags.fmt.timeZone


 # /root/jenkins
    root@kpismain:~/jenkins# pwd
    /root/jenkins
     
    root@kpismain:~/jenkins# ll
    total 16
    drwxr-xr-x  3 root root 4096 Sep 30 10:44 ./
    drwx------ 20 root root 4096 Sep 30 10:44 ../
    -rw-r--r--  1 root root  258 Sep 30 10:39 docker-compose.yml
    drwxrwxrwx 12 root root 4096 Sep 30 10:42 jenkins/
    root@kpismain:~/jenkins#

 
 
 #  vi docker-compose.yml

    
    version: '3'
    services:
      jenkins:
        container_name: 'jenkins'
        image: 'jenkins/jenkins:latest'
        restart: always
        ports:
          - 8081:8080
          - 50001:50000
        volumes:
          - ./jenkins:/var/jenkins_home
        environment:
          TZ: "Asiz/Seoul"
    ~

 # chmod -R 777 jenkins
 
 # docker compose up -d
 
 #  docker compose down
    
         
    root@kpismain:~/jenkins# ll
    total 16
    drwxr-xr-x  3 root root 4096 Sep 30 10:40 ./
    drwx------ 20 root root 4096 Sep 30 10:39 ../
    -rw-r--r--  1 root root  258 Sep 30 10:39 docker-compose.yml
    drwxrwxrwx 12 root root 4096 Sep 30 10:42 jenkins/
    root@kpismain:~/jenkins#


    
    
    drwxrwxrwx 12 root root 4096 Sep 30 10:48 jenkins/
    root@kpismain:~/jenkins# cd jenkins/
    root@kpismain:~/jenkins/jenkins# ll
    total 76
    drwxrwxrwx 12 root   root   4096 Sep 30 10:48 ./
    drwxr-xr-x  3 root   root   4096 Sep 30 10:48 ../
    drwxr-xr-x  3 master master 4096 Sep 30 10:42 .cache/
    -rw-r--r--  1 master master 1661 Sep 30 10:48 config.xml
    -rw-r--r--  1 master master  102 Sep 30 10:48 copy_reference_file.log
    -rw-r--r--  1 master master  156 Sep 30 10:48 hudson.model.UpdateCenter.xml
    drwxr-xr-x  3 master master 4096 Sep 30 10:42 .java/
    -rw-r--r--  1 master master  171 Sep 30 10:42 jenkins.telemetry.Correlator.xml
    drwxr-xr-x  2 master master 4096 Sep 30 10:42 jobs/
    -rw-r--r--  1 master master    0 Sep 30 10:48 .lastStarted
    -rw-r--r--  1 master master  907 Sep 30 10:48 nodeMonitors.xml
    drwxr-xr-x  2 master master 4096 Sep 30 10:42 nodes/
    drwxr-xr-x  2 master master 4096 Sep 30 10:42 plugins/
    -rw-r--r--  1 master master  129 Sep 30 10:48 queue.xml.bak
    -rw-r--r--  1 master master   64 Sep 30 10:42 secret.key
    -rw-r--r--  1 master master    0 Sep 30 10:42 secret.key.not-so-secret
    drwx------  2 master master 4096 Sep 30 10:42 secrets/
    drwxr-xr-x  2 master master 4096 Sep 30 10:48 updates/
    drwxr-xr-x  2 master master 4096 Sep 30 10:42 userContent/
    drwxr-xr-x  3 master master 4096 Sep 30 10:42 users/
    drwxr-xr-x 10 master master 4096 Sep 30 10:42 war/
    root@kpismain:~/jenkins/jenkins#



# initialAdminPassword
    
    root@kpismain:~/jenkins/jenkins# docker container exec -it jenkins bash
    jenkins@6f0f08a5db8c:/$ pwd
    /
    jenkins@6f0f08a5db8c:/$ cd /var/jenkins_home/
    jenkins@6f0f08a5db8c:~$ ll
    bash: ll: command not found
    jenkins@6f0f08a5db8c:~$ ls
    config.xml               hudson.model.UpdateCenter.xml     jobs              nodes    queue.xml.bak  secret.key.not-so-secret  updates      users
    copy_reference_file.log  jenkins.telemetry.Correlator.xml  nodeMonitors.xml  plugins  secret.key     secrets                   userContent  war
    jenkins@6f0f08a5db8c:~$ cd secret
    bash: cd: secret: No such file or directory
    jenkins@6f0f08a5db8c:~$ cd secrets/
    jenkins@6f0f08a5db8c:~/secrets$ ll
    bash: ll: command not found
    jenkins@6f0f08a5db8c:~/secrets$ ls
    initialAdminPassword  jenkins.model.Jenkins.crumbSalt  master.key
    jenkins@6f0f08a5db8c:~/secrets$ cat initialAdminPassword
    e283b74f77014266814da8a98d983804
    jenkins@6f0f08a5db8c:~/secrets$ pwd
    /var/jenkins_home/secrets



