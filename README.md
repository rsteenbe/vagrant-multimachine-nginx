# Vagrant Multimachine (2 Nginx separate application servers)
Two vagrant boxes running Nginx application servers.

## Installation
## Windows 7
Before running the box download [Vagrant](https://www.vagrantup.com/) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

Run the following command in the command prompt:

`vagrant up --provider=virtualbox`

After the installation, enter the following URL in the browser to see if both servers are working:

Nginx Server 1:
http://localhost:80

Nginx Server 2:
http://localhost:81

To access the backend, enter in the command line:
`vagrant ssh server1` or `vagrant ssh server2`
