# postgis_pgadmin
PostGIS and PGAdmin configuration

Clone or Download this repository to your local drive

You must have Docker Desktop installed in your OS.
Get Docker Desktop from https://www.docker.com/products/docker-desktop/

This repository contains PostGIS and PGAdmin.
To run the PGAdmin and PostGIS

$ docker compose up

Once the services are running, you need to connect the PGAdmin and PostGIS
Check the network bridge connection in Docker.
Open a new terminal, navigate to this project folder.

Check the network connection:
$ docker network ls

find XXXX_default is the default bridge network that connect PostGIS and PGAdmin
Run the following script to obtain the ip address for the PostGIS server

$ docker network inspect XXXX_default

This is the example of network bridge configuration
        "ConfigOnly": false,
        "Containers": {
            "7e957c975fe0954f4d794582bde84ffbd9025126a70c7f602b74097d1f9e6a4d": {
                "Name": "postgis-pgadmin-1",
                "EndpointID": "4fd3c18a130a577dcc614316f2a7aed7ca670eb8153d267e4157812b89a0608b",
                "MacAddress": "02:42:ac:14:00:03",
                "IPv4Address": "172.20.0.3/16",
                "IPv6Address": ""
            },
            "f26456e8fd29b226a163ecb21e36733f59abefaf5bc4f6a83738738f8ddb5591": {
                "Name": "postgis-db-1",
                "EndpointID": "25c3f156b8955783e4f7480ce5b6cd174f1e3f938c6cc73b7871ddd117060739",
                "MacAddress": "02:42:ac:14:00:02",
                "IPv4Address": "172.20.0.2/16",
                "IPv6Address": ""
            }
        },
        
In this example, the PostGIS server is running at 172.20.0.2
use this IP address to connect to the PostGIS server from the PGAdmin.
The database username, password and database name are available in docker-compose.yml

Created for CSE3DMS by kiki adhinugraha
