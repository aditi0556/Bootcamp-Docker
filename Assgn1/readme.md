# Assignment 1
 There is an index.html file 
 A dockerfile is created and a base image nginx is chosen, an index.html file is copied .
 Image is created using     ### docker build -t aditisinha-site:latest . 
 Then a container is started and port is exposed to the host using the command  
  ### docker run -d --name assgn1 -p 7070:80 aditisinha-site:latest
 Now at http://localhost:7070 <img width="1441" height="551" alt="image" src="https://github.com/user-attachments/assets/ce3a58fc-1e56-4042-8736-0c18da78f80b" />



 # Assignment 2
  There are two containers in the network webnet.  
  used ### docker network create webnet
  Then created a container named api exposed at port 5678 using built in image hashicorp/http-echo
  Then image is build using nginx as the base image , configured the default.conf file 
  Here in the default.conf file nginx is acting as a reverse proxy for req at /api , and at / index.html page is accessed which has a btn which routes to /api
  Image is build using docker build command and then a container is started where the 8000 is exposed to the host

  
  ### docker build -t aditi .
  ### docker run -d --name tmp --network webnet -p 8000:8000 aditi
  ### docker exec -it tmp curl http://api:5678
 <img width="1424" height="496" alt="image" src="https://github.com/user-attachments/assets/43ea67a1-a226-4b72-a734-e968f7abcc44" />
 <img width="734" height="76" alt="image" src="https://github.com/user-attachments/assets/494f8953-f8d6-48bb-b7e8-17823fa147c9" />





