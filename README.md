# ssh-jenkins-test
jenkins controller, jenkins node and db2 server infrastructure for ssh test

## steps  
  - create ubuntu server for jenkins controller - docker based deployemnt  
  - create ubuntu server for jenkins node - docker based
  - creat AWS Linux server for DB2 installation
  - create a jenkins pipline to use a linux agen to deploy DB2 database on the db2 server

Using eu-west-2 region

## configuration
 - increase the size of the swap file on all servers to 1 gb  
 ```
 sudo fallocate -l 1G /var/swapfile
 sudo chmod 600 /var/swapfile
 sudo mkswap /var/swapfile
 sudo swapon /var/swapfile
 echo '/var/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
 sudo sysctl -p
 ```