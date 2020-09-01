FROM centos:7

# MAINTAINED by ramukunireddy
# installs ping, netstat for debugging purposes
# installing tzdata will fix NESSUS_TZ_DIR related warning

RUN yum -y install net-tools lsof tzdata

RUN rm -rf /var/lib/apt/lists/*

COPY Nessus-8.11.1-es7.x86_64.rpm /tmp/nessus.rpm

RUN rpm -ivh /tmp/nessus.rpm

# defaut Nessus Scanner port
EXPOSE 8834

CMD [ "/opt/nessus/sbin/nessus-service" ]
# ENTRYPOINT [ "/etc/init.d/nessusd start" ]
