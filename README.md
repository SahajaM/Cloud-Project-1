# Cloud-Project-1

# Installing docker
$ sudo yum update -y 

$ sudo yum install -y docker

$ sudo service docker start

# Now create a directory name cloud and place requirements.txt, forecast.py, Dockerfile, daily.csv and templates folder which contains try.html

# Created a Docker image by using the command
docker build -t weatherforecast

# Run the code by mapping machine port 80 to container's published port 80 using -p
docker run -p 80:80 -t weatherforecast

# The following commands are generally used in docker,
To see active images running
docker ps
To stop the active image
docker stop <imageid>
To destory all images and container
docker system prune

# To create an account in cloud.docker.com
docker login

# To run the docker tag image with your username, repository and tag names to upload the image to desired destination
docker tag weatherforecast sahaja99/cloudproject:final

# To upload tagged image to repository
docker push sahaja99/cloudproject:final

# To run docker app on any machine use the command
docker run -p 80:80 sahaja99/cloudproject:final
