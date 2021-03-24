# Ansible-roles_httpd_haproxy_LB
### Task Description📄

🔅Create an ansible role myapache to configure Httpd WebServer.
🔅Create another ansible role myloadbalancer to configure HAProxy LB.
🔅We need to combine both of these roles controlling webserver versions  and solving challenge for host ip's  addition  dynamically over  each  Managed Node  in  HAProxy.cfg file.

#### Solution:
##### roles:
myapache role : Configure httpd 
variables used :  1. p : package name  (default httpd)
                  2. path : path to put web pages (default /var/www/html)
                  3. ser_name  : name of service (default httpd)
                  4. port : port on which httpd host the web (default 80)


mylb role :  Configure haproxy Load Balancer
variables used :  1. pkg_name: package name  (default haproxy)
                  2. dest_path: path of configuration file of haproxy (default /etc/haproxy/haproxy.cfg)
                  3. ser_name : name of service (default haproxy)
                  4. port : port of Load Load blancer  (default 8082)
yum role : configure yum in BaseOS (iso image should attached to OS)
variables used :  1. dir_path:  path to mount the cdrom (example = /dvd10")
                 

##### Playbook: 
setup.yml :  roles is excuted using this playbook
removesetup.yml : to remove setup.yml's Playbook configuration

### NOTE: if this roles exected on AWS , DO comment the YUM role in setup.yml !!!

