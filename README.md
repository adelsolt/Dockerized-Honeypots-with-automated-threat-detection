# Dockerized-Honeypots-with-automated-threat-detection
Dockerized security environment featuring Cowrie honeypots, Suricata for real-time IDS, and an ELK Stack for centralized logging and attack visualization via Kibana.

## Project Overview

This project is a Docker-based honeypot setup designed to attract and log malicious activity. I uses Docker and Docker Compose to create and deploy both Suricata and Cowrie honeypots containers and The ELK container. The project includes:

    Cowrie: SSH and Telnet honeypot to log attacker interactions.
    Suricata: Intrusion Detection System (IDS) to monitor network traffic for suspicious behavior.
    ELK Stack: Elasticsearch, Logstash, and Kibana for log analysis and visualization.

My goal in this project is to practice deploy security infrastructure using Docker to simulate real-world cyberattacks attacks for analysis.

## Project Components

    Cowrie Honeypot container: Logs all SSH and Telnet interactions from attackers (usernames, passwords, and commands).
    Suricata IDS container: Monitors network traffic and generates alerts for suspicious activity.
    ELK Stack container: Visualizes the logs from honeypots and Suricata, providing a centralized dashboard for monitoring.
    Debian 12 VM running in VMware which will be the host for the Docker Containers.
    Windows 11 (host system) for accessing the honeypots and Kibana dashboard.

## Networking

I have created a dedicated bridged network for the docker conatiners in order to communicate with each others with 

```
docker network create logging-network
```


Check container logs for issues:

    docker logs suricata
    docker logs cowrie
    docker logs elk

8. Test and Optimize

    Confirm that logs from Suricata and Cowrie are visible in Kibana.
    Fine-tune configurations for performance and alerting.

Let me know if you need clarification on any step!