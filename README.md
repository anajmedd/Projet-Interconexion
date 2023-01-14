<div class="logo"><img src="Docker.png" width="250px" align="right"></div>


#  Interconnection of autonomous services

## Table of Contents

- [About](#about)
- [Run](#run)
- [License](#license)

## About

<p>This project demonstrates the interconnection of autonomous services using Docker. The project includes multiple microservices that communicate with each other to perform a specific task. Each service is packaged and deployed as a Docker container, allowing for easy scaling and management of the services. The project also includes scripts and configurations for setting up a Docker network and running the services in a coordinated manner.</p>


## Run

In a GitBash, type :
                ```git clone https://github.com/anajmedd/Projet-Interconexion.git```

Open a terminal, and type :<br>

        cd Projet-Interconnexion/
	chmod +x projet.sh
	./projet.sh

Here servals dockers will appear representing the whole architecture of our AS 
(Client, DHCP server, routers and servers, etc...).<br>
To stop the dockers, you have to type :<br>

	docker kill  $(docker ps -a -q)  
  
Then, type :<br>

	docker rm  $(docker ps -a -q)
	docker rmi  $(docker images -a -q)
## License

The library is Software released under Apache-2.0 [License](LICENSE.txt).
