# LAB3_TOPICOS-TELEMATICA
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#how-work">How work</a></li>
    <li><a href="#setup">Setup</a></li>
        <ol>
            <li><a href="#docker">Docker</a></li>
            <li><a href="#nginx-1">Nginx</a></li>
            <li><a href="#react">React</a></li>
            <li><a href="#express">ExpressJs</a></li>
            <li><a href="#mongodb">Mongodb</a></li>
        </ol>
    <li><a href="#demo">Demo</a></li>     
  </ol>
</details>



## How work


![Web App Reference Architecture](https://user-images.githubusercontent.com/53051443/164953484-52bef134-c773-47ea-ae68-cb9db69c70d9.png)


### Front and Back

The BookStore front and back is provided by the teacher jcmontoy@eafit.edu.co and build it on docker containers.

### Mongo

The database Mongodb is the Community version running local on AWS EC2 Machine

### Nginx 
Nginx is working on another AWS EC2 machine working as proxy

## Setup 

### Nginx

Nginx is the same configuration as the last Lab 



### React

The main reason to use docker is to isolate the dependences to avoid problems on the EC2 Machine, react will use docker-compose and Dockerfile when the machine starts or the container fails restart automatically, Dockerfile and docker-compose are located on this repo on frontend folder.

When everthing is done please run this command where is located your docker-compose.yml 

```bash
sudo docker-compose up -d
```

### Express

```bash
sudo docker-compose up -d
```

### Mongodb

Follow the guide provided by Mongodb team to install Mongodb Community edition on your AWS EC2 Machine [Setup Mongo](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/) 


#### Connect to database

To connect to the database on the backend using mongoose the database url look like this

```bash
mongo "mongodb://${DBUSER}:${DBPASSWORD}@<host>:<port>/<dbname>?authSource=admin"
```

## Demo 

[Visit Bookstore](https://bibliotecadondepacho.tk/) 

When you visit the webpage you will see 

<img width="960" alt="image" src="https://user-images.githubusercontent.com/53051443/164952919-95e86be6-99fa-40ef-bd9e-86aa02f8576f.png">
