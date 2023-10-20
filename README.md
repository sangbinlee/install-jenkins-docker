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



      
      root@master:~/jenkins# docker compose ps -a
      NAME      IMAGE     COMMAND   SERVICE   CREATED   STATUS    PORTS
      root@master:~/jenkins# ll
      total 16
      drwxr-xr-x  3 root root 4096 Oct 21 01:44 ./
      drwx------ 14 root root 4096 Oct 21 01:21 ../
      -rw-r--r--  1 root root  369 Oct 21 00:30 docker-compose.yml
      drwxr-xr-x  2 root root 4096 Oct 21 01:44 jenkins/
      root@master:~/jenkins# chmod -R 777 ./jenkins/
      root@master:~/jenkins# ll
      total 16
      drwxr-xr-x  3 root root 4096 Oct 21 01:44 ./
      drwx------ 14 root root 4096 Oct 21 01:21 ../
      -rw-r--r--  1 root root  369 Oct 21 00:30 docker-compose.yml
      drwxrwxrwx  2 root root 4096 Oct 21 01:44 jenkins/
      root@master:~/jenkins#
      
      
      
      







 
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


# docker compose up
    
    
    root@master:~/jenkins# ll
    total 16
    drwxr-xr-x  3 root root 4096 Oct 21 01:44 ./
    drwx------ 14 root root 4096 Oct 21 01:21 ../
    -rw-r--r--  1 root root  369 Oct 21 00:30 docker-compose.yml
    drwxrwxrwx  2 root root 4096 Oct 21 01:44 jenkins/
    root@master:~/jenkins# docker compose up
    [+] Running 1/0
     ✔ Container jenkins  Created                                                                                                                0.1s
    Attaching to jenkins
    jenkins  | Running from: /usr/share/jenkins/jenkins.war
    jenkins  | webroot: /var/jenkins_home/war
    jenkins  | 2023-10-20 16:53:27.436+0000 [id=1]  INFO    winstone.Logger#logInternal: Beginning extraction from war file
    jenkins  | 2023-10-20 16:53:28.457+0000 [id=1]  WARNING o.e.j.s.handler.ContextHandler#setContextPath: Empty contextPath
    jenkins  | 2023-10-20 16:53:28.535+0000 [id=1]  INFO    org.eclipse.jetty.server.Server#doStart: jetty-10.0.17; built: 2023-10-02T04:04:10.314Z; g                          it: a0f5f05abaa6c3aabb7c3d35f10a6f412ab8b05f; jvm 17.0.8.1+1
    jenkins  | 2023-10-20 16:53:28.843+0000 [id=1]  INFO    o.e.j.w.StandardDescriptorProcessor#visitServlet: NO JSP Support for /, did not find org.e                          clipse.jetty.jsp.JettyJspServlet
    jenkins  | 2023-10-20 16:53:28.900+0000 [id=1]  INFO    o.e.j.s.s.DefaultSessionIdManager#doStart: Session workerName=node0
    jenkins  | 2023-10-20 16:53:29.421+0000 [id=1]  INFO    hudson.WebAppMain#contextInitialized: Jenkins home directory: /var/jenkins_home found at:                           EnvVars.masterEnvVars.get("JENKINS_HOME")
    jenkins  | 2023-10-20 16:53:29.548+0000 [id=1]  INFO    o.e.j.s.handler.ContextHandler#doStart: Started w.@4d8286c4{Jenkins v2.428,/,file:///var/j                          enkins_home/war/,AVAILABLE}{/var/jenkins_home/war}
    jenkins  | 2023-10-20 16:53:29.564+0000 [id=1]  INFO    o.e.j.server.AbstractConnector#doStart: Started ServerConnector@37ddb69a{HTTP/1.1, (http/1                          .1)}{0.0.0.0:8080}
    jenkins  | 2023-10-20 16:53:29.579+0000 [id=1]  INFO    org.eclipse.jetty.server.Server#doStart: Started Server@43aaf813{STARTING}[10.0.17,sto=0]                           @2751ms
    jenkins  | 2023-10-20 16:53:29.581+0000 [id=26] INFO    winstone.Logger#logInternal: Winstone Servlet Engine running: controlPort=disabled
    jenkins  | 2023-10-20 16:53:29.873+0000 [id=34] INFO    jenkins.InitReactorRunner$1#onAttained: Started initialization
    jenkins  | 2023-10-20 16:53:29.892+0000 [id=32] INFO    jenkins.InitReactorRunner$1#onAttained: Listed all plugins
    jenkins  | 2023-10-20 16:53:30.993+0000 [id=34] INFO    jenkins.InitReactorRunner$1#onAttained: Prepared all plugins
    jenkins  | 2023-10-20 16:53:30.999+0000 [id=35] INFO    jenkins.InitReactorRunner$1#onAttained: Started all plugins
    jenkins  | 2023-10-20 16:53:31.008+0000 [id=35] INFO    jenkins.InitReactorRunner$1#onAttained: Augmented all extensions
    jenkins  | 2023-10-20 16:53:31.266+0000 [id=39] INFO    jenkins.InitReactorRunner$1#onAttained: System config loaded
    jenkins  | 2023-10-20 16:53:31.267+0000 [id=39] INFO    jenkins.InitReactorRunner$1#onAttained: System config adapted
    jenkins  | 2023-10-20 16:53:31.268+0000 [id=39] INFO    jenkins.InitReactorRunner$1#onAttained: Loaded all jobs
    jenkins  | 2023-10-20 16:53:31.270+0000 [id=39] INFO    jenkins.InitReactorRunner$1#onAttained: Configuration for all jobs updated
    jenkins  | 2023-10-20 16:53:31.346+0000 [id=52] INFO    hudson.util.Retrier#start: Attempt #1 to do the action check updates server
    jenkins  | 2023-10-20 16:53:31.841+0000 [id=35] INFO    jenkins.install.SetupWizard#init:
    jenkins  |
    jenkins  | *************************************************************
    jenkins  | *************************************************************
    jenkins  | *************************************************************
    jenkins  |
    jenkins  | Jenkins initial setup is required. An admin user has been created and a password generated.
    jenkins  | Please use the following password to proceed to installation:
    jenkins  |
    jenkins  | 7212fcf0c0204c0ea6a03b60a8df7d0e
    jenkins  |
    jenkins  | This may also be found at: /var/jenkins_home/secrets/initialAdminPassword
    jenkins  |
    jenkins  | *************************************************************
    jenkins  | *************************************************************
    jenkins  | *************************************************************
    jenkins  |
    jenkins  | 2023-10-20 16:53:51.245+0000 [id=34] INFO    jenkins.InitReactorRunner$1#onAttained: Completed initialization
    jenkins  | 2023-10-20 16:53:51.261+0000 [id=25] INFO    hudson.lifecycle.Lifecycle#onReady: Jenkins is fully up and running
    jenkins  | 2023-10-20 16:53:52.119+0000 [id=52] INFO    h.m.DownloadService$Downloadable#load: Obtained the updated data file for hudson.tasks.Maven.MavenInstaller
    jenkins  | 2023-10-20 16:53:52.120+0000 [id=52] INFO    hudson.util.Retrier#start: Performed the action check updates server successfully at the attempt #1










![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/f6a37f74-19ed-457b-9e91-4f26742c8364)





![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/dd47698f-5f90-4f81-b723-3d2cd3223130)

![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/26542255-eea6-48eb-876c-2fcd27e1d257)



![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/444b2f27-15bd-45fd-92c8-b2d8d37883ac)




# example
    sudo mkdir -p /private/var/jenkins_home
    sudo chown -R 1000:1000 /private/var/jenkins_home

    docker run -d -p 8080:8080 -p 50000:50000 -v /private/var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --name jenkins maole01/jenkins

![image](https://github.com/sangbinlee/install-jenkins-docker/assets/4024414/6b5dc8a2-f06f-45be-9da5-24d3024d8c22)

    ERROR ON AWS #INSTANCE### i have tried its working
    touch: cannot touch /var/jenkins_home/copy_reference_file.log: Permission denied
    while installing jenkins from docker image . By defalut jenkins user is create
    so create create a dir
    
    mkdir /var/jenkins_home
    chmod 777 /var/jenkins_home
    chown jenkins:jenkins /var/jenkins_home
    docker run --name jenkins-test -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home jenkins

