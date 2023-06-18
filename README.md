# final group-project
# FURKAN BEKTAŞ 21832971
## harita.hacettepe.edu.tr
It is a project in which the map web-service of Hacettepe University is shared openly.

First, I downloaded the codes via https://github.com/banbar/harita.hacettepe.edu.tr.
![image](https://github.com/jungry1/readme/assets/66970973/69c80ec0-4883-439e-9402-c97feb25469b)

# Requirements for running the Hacettepe Campus project:
-PostgreSql 
-Node.js
-Visual Studio Code

I transferred the SQL code to the postgresql software with the restore command (database: hacettepecampus). I then connected the postgis and qgis apps. In this way, I transferred the postgis layers to qgis.

![image](https://github.com/jungry1/readme/assets/66970973/383a1444-2168-476a-8f1f-2b3f9c1962a9)
![image](https://github.com/jungry1/readme/assets/66970973/71d8bf98-9d3a-45f3-80a5-923eced906ae)

After installing the libraries, I connected to the server platform. To use the NPM module, we need to install the node.js application. We connect to localhost by entering our own postgresql host information in the db part of the code.

![image](https://github.com/jungry1/readme/assets/66970973/5a4e4ac0-701a-46a4-b984-b1b1c5f02f52)

![image](https://github.com/jungry1/readme/assets/66970973/f6936132-164c-4b8b-9711-8645c1473e4a)


Then, using the same commands on the client, we connect to the frontend (Hacettepe campus).

![image](https://github.com/jungry1/readme/assets/66970973/1147c9ea-96fb-4bce-b9b4-964d987d3a53)

## BOUNDING BOX IN QGIS 
In QGIS, a bounding box refers to a rectangular area that defines the spatial extent of a geographic feature or a set of features. It is represented by four coordinates: the minimum and maximum values for both the x-axis (longitude or easting) and the y-axis (latitude or northing). 

First, we install the lat lon tools and bounding box plugins from the plugin section of qgis. Then we enter the BBOX Capture section from the lat lon tools > settings section. Here we enter the projection as our format (xmin, ymin, xmax, ymax). After completing the process, we receive the coordinate information.
![image](https://github.com/jungry1/readme/assets/66970973/7144430a-ec40-4207-8b7a-b4d0d4e5eaf2)

Then we create a new postgresql table. In this table we enter the boundingbox coordinates. Here we choose the numeric data type to enter the coordinates because our coordinates are decimal numbers. We will update this information in the code in the next stages.
![image](https://github.com/jungry1/readme/assets/66970973/bc390e30-d2cd-4819-9820-98e321e5f0df)
![image](https://github.com/jungry1/readme/assets/66970973/f87c267d-ffd3-461a-b54f-c7044f188216)

Before pulling the code in Postgresql, you need to update your localhost information from the db.js section.
![image](https://github.com/jungry1/readme/assets/66970973/fc4fdbac-9d4b-4d12-addb-5730b0d564b2)

I updated the code with the app.get command to pull the table in Postgresql.
![image](https://github.com/jungry1/readme/assets/66970973/89c11f91-66c1-4c59-8b4e-0cc3f9e0d161)














