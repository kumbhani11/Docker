# Docker

Download Docker desktop from here <a href='https://docs.docker.com/desktop/install/windows-install/'>Docker Downloader</a>
install the software and keep open

<h3>Create Docker Compose File for Database [Backend]</h3>

Create Folder where you want to create project. eg: D:/docker_project

Open cmd and create image by following command

<code>docker pull mongo && docker pull mongo-express</code>

now download file <code>docker_composer.yml</code> and store in under created folder i.e. /docker_project

now run <code>docker_composer.yml</code> file from cmd to connect with database

<code>D:/docker_project>docker-compose -f docker_composer.yml up</code>

Now you can check in Docker Desktop Application running Container.  

<code>Output</code>

![Container](https://user-images.githubusercontent.com/51017576/204712798-b10b08ed-9be3-4254-bea3-83a8ab9b45bb.png)

