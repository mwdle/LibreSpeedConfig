# LibreSpeed Docker Compose Configuration  

A sample Docker Compose file for LibreSpeed.  

## Important Details

* The Docker Compose file assumes you have already created a Docker network called ```Speedtest```. You can create this network before starting the container by executing the following command: ```docker network create Speedtest```  
* You must change the ```DOCKER_VOLUMES``` path in the ```.env``` file to a folder on your system where you wish to store container files (used in Docker Compose bind mounts).  

## Starting the container  

In your terminal, ```cd``` to the directory containing the ```docker-compose.yml``` and ```.env``` files. Run the following command: ```docker compose up -d```  
Your containers should be up and running and your LibreSpeed instance be accessible on port 80 and 443 in the container. Setup your Docker Networks and reverse proxy accordingly.  

## Disclaimer  

This repository is provided as-is and is intended for informational and reference purposes only. The author assumes no responsibility for any errors or omissions in the content or for any consequences that may arise from the use of the information provided. Always exercise caution and seek professional advice if necessary.  
