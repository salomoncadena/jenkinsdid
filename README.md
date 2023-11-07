# jenkinsdid
Jenkins with Docker in Docker

# Build image
docker build . -t jenkins/jenkins:did

# Run Jenkins Docker in Docker
docker run -u 0 -d -p 80:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock -v /opt/jenkins/jenkins_home:/var/jenkins_home jenkins/jenkins:did
