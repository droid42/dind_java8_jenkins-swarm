dind_java8_jenkins-swarm
========================

Jenkins-Swarm Slave from Docker in Docker with Java8

You can use Docker in your builds to create new images, launch containers and push the images to (your) registry.

Run the jenkins-slave with:
	docker run -ti --privileged --rm \
	-e JENKINS_MASTER=http://<your-jenkins-ip>:<your-jenkins-port> \
	-e JENKINS_USERNAME='jenkins' \
	-e JENKINS_PASSWORD='jenkins' \
	-e SLAVE_NAME="DockerSlave" \ 
	-e SLAVE_LABELS="Docker Java8" \
	-e SLAVE_EXECUTORS=2 \
	-e SLAVE_MODE=exclusive \
	droid42/dind-java8-jenkins-swarm
