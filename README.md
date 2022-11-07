# Docker-Kafka-2-SplunkEE

This is a fork of https://github.com/guilhemmarchand/kafka-docker-splunk that trims down the larger original lab and provides a minimal environment to allow the testing/proof of concept of sending data from a Zookeeper-Kafka instance/cluster to Splunk Enterprise Edition.

While the original lab provides 2 options for hosting Splunk (local instance on host or on docker), this proof of concept focuses only on using Docker. The goal is that with 1 clone command and 1 docker compose up command you are ready to go after a few minutes, and can see Kafka data in the Splunk instance. 

Prerequisites: 
      
      - Docker Desktop (Windows) or Docker Engine (Linux) 
      - Docker Compose (if not already packaged with Docker)
      - OpenSSH-server (optional)

How to Use:

      - Clone the repository, and CD to the /docker directory.
      - Use "sudo ./run.sh" to download the necessary containers and set up the lab.
      - Connect to localhost:8000, and log in to Splunk using "admin/ch@ngeM3".
      - On the left side (installed apps), select "Kafka Smart Monitoring"
      - You should be seeing "REALTIME AVG TRAFFIC IN (Kbps in)" and "REALTIME AVG MESSAGES/IN SEC" being received from kafka-1
