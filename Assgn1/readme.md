# Assignment 1
 There is an index.html file 
 A dockerfile is created and a base image nginx is chosen, an index.html file is copied .
 Image is created using     ### docker build -t aditisinha-site:latest . 
 Then a container is started and port is exposed to the host using the command  
  ### docker run -d --name assgn1 -p 7070:80 aditisinha-site:latest
 Now at http://localhost:7070 <img width="1706" height="537" alt="image" src="https://github.com/user-attachments/assets/bb2499b1-f753-46f6-9278-70d1fd0e05d4" />
 

 #Assignment 2
  There are two containers in the network webnet.  
  used ### docker network create webnet
  Then created a container named api exposed at port 5678 using built in image hashicorp/http-echo
  Then image is build using nginx as the base image , configured the default.conf file 
  Here in the default.conf file nginx is acting as a reverse proxy for req at /api , and at / index.html page is accessed which has a btn which routes to /api
  Image is build using docker build command and then a container is started where the 8000 is exposed to the host
  ### docker build -t aditi .
  ### docker run -d --name tmp --network webnet -p 8000:8000 aditi
  ### docker exec -it tmp curl http://api:5678
 <img width="811" height="101" alt="image" src="https://github.com/user-attachments/assets/40b11d97-8d9c-4718-a09b-344b573dc533" />
 <img width="1527" height="549" alt="image" src="https://github.com/user-attachments/assets/28bb5799-ec05-4024-bfd8-07a25b4a699e" />


