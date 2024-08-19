# LibreSpeed Docker Compose Configuration  

A sample Docker Compose file for LibreSpeed.  

## Table of Contents  

* [Description](#librespeed-docker-compose-configuration)  
* [Getting Started](#getting-started)  
* [License](#license)  
* [Disclaimer](#disclaimer)  

## Getting Started  

1. Clone the repository:  

    ```shell
    git clone https://github.com/mwdle/LibreSpeedConfig.git
    ```  

2. Create a folder on your system for Docker bind mounts / storing container files. The folder should have the following structure:  

    ```shell
    docker_volumes/
    ├── Speedtest/
    │   └── config/
    ```  

3. Change the ```.env``` file properties for your configuration:  

    ```properties
    DOCKER_VOLUMES=<PATH_TO_DOCKER_VOLUMES_FOLDER> # The folder created in the previous step.
    ```  

4. Open a terminal in the directory containing the docker-compose file.  
5. Create a docker network for the container:  

    ```shell
    docker network create Speedtest
    ```  

6. Start the container:  

    ```shell
    docker compose up -d
    ```  

Your container should be up and running and your LibreSpeed instance be accessible on port 80 and 443 in the container. Attach your reverse proxy container to the previously created Docker Networks and configure it accordingly.  

## License  

This project is licensed under the GNU General Public License v3.0 (GPL-3.0). See the [LICENSE](LICENSE.txt) file for details.  

## Disclaimer  

This repository is provided as-is and is intended for informational and reference purposes only. The author assumes no responsibility for any errors or omissions in the content or for any consequences that may arise from the use of the information provided. Always exercise caution and seek professional advice if necessary.  
