# Docker

Download Docker desktop from here <a href='https://docs.docker.com/desktop/install/windows-install/'>Docker Downloader</a>
install the software and keep open

<h3>Create Docker Compose File for Database [Backend]</h3>

<h4>Method 1</h4>
Create Folder where you want to create project. eg: D:/docker_project

Open cmd and create image by following command

<code>docker pull mongo && docker pull mongo-express</code>

now download file <code>docker_composer.yml</code> and store in under created folder i.e. /docker_project

now run <code>docker_composer.yml</code> file from cmd to connect with database

<code>D:/docker_project>docker-compose -f docker_composer.yml up</code>

Now you can check in Docker Desktop Application running Container.  

<code>Output</code>

![Container](https://user-images.githubusercontent.com/51017576/204712798-b10b08ed-9be3-4254-bea3-83a8ab9b45bb.png)

<h4>Method 2</h4>

We can run service through cmd.

create image
	docker pull mongo && docker pull mongo-express

create network. network is bridge between mongo and mongo-express
```docker create network mongo-network```

create container
	```docker run -d -p 27017:27017  -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo```
	659e600001d331d9f28987d890f432dd36266d7a0a74a7cf6c719c3d96d3855d```

	```docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb  mongo-express```
	28a9159d2f5ef3b50d7388bbf1f5fe67df3bfa839c515c77b885a5c82cf6efbf
  
  running this command yit will return some unique id. it means service is running successfully.
  
  You can check running service in Docker Desktop Application.
  
  Thank you
  
  
  
