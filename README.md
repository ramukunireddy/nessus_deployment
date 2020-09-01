# nessus_deployment
-->To deploy nessus .rpm file in centos 7 and running it through docker:

        git clone https://github.com/ramukunireddy/nessus_deployment
        cd nessus_deployment

-->Execute below commans to build docker image and start nessus Container:
         $docker build --build-arg rpmfile=Nessus-8.11.1-es7.x86_64.rpm -t nessus .

-->Get the mac ip by running using : ifconfig 
        And copy the map address

-->Start the Nessus Docker container:
        docker run -d --name nessus -p 8834:8834 --mac-address <macAddress> centos7/nessus /opt/nessus/sbin/nessus-service

-->Execute below commans to view list of running containers:
         $ docker ps

-->Access the url from ur mac using 
        https://clusterip:8834




