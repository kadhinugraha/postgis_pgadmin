<html>
# postgis_pgadmin<br>
PostGIS and PGAdmin configuration<br>
<br>
Clone or Download this repository to your local drive<br>
<br>
You must have Docker Desktop installed in your OS.<br>
Get Docker Desktop from https://www.docker.com/products/docker-desktop/<br>
<br>
This repository contains PostGIS and PGAdmin.<br>
To run the PGAdmin and PostGIS<br>
<br>
$ docker compose up<br>
<br>
Once the services are running, you need to connect the PGAdmin and PostGIS<br>
Check the network bridge connection in Docker.<br>
Open a new terminal, navigate to this project folder.<br>
<br>
Check the network connection:<br>
$ docker network ls<br>
<br>
find XXXX_default is the default bridge network that connect PostGIS and PGAdmin<br>
Run the following script to obtain the ip address for the PostGIS server<br>
<br>
$ docker network inspect XXXX_default<br>
<br>
This is the example of network bridge configuration<br>
<br>        "ConfigOnly": false,
<br>        "Containers": {
<br>            "7e957c975fe0954f4d794582bde84ffbd9025126a70c7f602b74097d1f9e6a4d": {
<br>                "Name": "postgis-pgadmin-1",
<br>                "EndpointID": "4fd3c18a130a577dcc614316f2a7aed7ca670eb8153d267e4157812b89a0608b",
<br>                "MacAddress": "02:42:ac:14:00:03",
<br>                "IPv4Address": "172.20.0.3/16",
<br>                "IPv6Address": ""
<br>            },
<br>            "f26456e8fd29b226a163ecb21e36733f59abefaf5bc4f6a83738738f8ddb5591": {
<br>                "Name": "postgis-db-1",
<br>                "EndpointID": "25c3f156b8955783e4f7480ce5b6cd174f1e3f938c6cc73b7871ddd117060739",
<br>                "MacAddress": "02:42:ac:14:00:02",
<br>                "IPv4Address": "172.20.0.2/16",
<br>                "IPv6Address": ""
<br>            }
<br>        },
<br>        <br>
In this example, the PostGIS server is running at 172.20.0.2<br>
use this IP address to connect to the PostGIS server from the PGAdmin.<br>
The database username, password and database name are available in docker-compose.yml<br>
<br>
Created for CSE3DMS by kiki adhinugraha<br>
</html>
