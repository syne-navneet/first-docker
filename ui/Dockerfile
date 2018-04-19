FROM centos:latest
MAINTAINER navneet.sharma@synechron.com
RUN yum -y update 
RUN mkdir /opt/config
ADD config /opt/config
RUN yum -y install `cat /opt/config/packages`
ADD code /var/www/html/
EXPOSE 80
# directly run as a process id:1
CMD ["apachectl", "-D", "FOREGROUND"] 
 

