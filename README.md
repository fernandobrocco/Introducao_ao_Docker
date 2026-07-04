# Voting API (TechVotos) - DevOps

This project was developed as a Final Integrative Project with the goal of packaging, automating, and monitoring a Python/Flask voting API. I isolated the application using Docker containers and configured the orchestration of the multi-service environment (App, Prometheus, and Grafana) via Docker Compose. 

It enables Prometheus to perform consecutive data scrapes every 5 seconds and Grafana to display visual dashboards for decision-making.

An integrative project to test knowledge in Docker and containerization, taught by Professor Eden Ricardo Dosciatti in the Software Automation and Infrastructure course.

## How to Run the Project (Step-by-Step)

To run the entire environment on your machine without having to manually configure Python or databases, you only need to have **Docker** and **Docker Compose** installed on your system.

1. **Download the Project:** Open the terminal on your machine, clone this repository using the command `git clone https://github.com/fernandobrocco/Docker_container_initialization.git` and navigate into the folder using `cd Docker_container_initialization`.

2. **Start the Infrastructure:** Run the command `docker compose up -d` to download the required images and start all services isolated in the background.

3. **Vote via the API:** Open your web browser and go to `http://localhost:5000/`. The voting system's homepage will be online. To cast votes and test how it works, you can directly access the addresses `http://localhost:5000/votar/a` or `http://localhost:5000/votar/b`.

4. **Check Prometheus Metrics:** To check if the data collector is working and communicating with the application, go to `http://localhost:9090/targets`. In the metrics section, enter `app_votos_total` to view the total number of votes between A and B.

5. **Access the Grafana Dashboard:** Go to `http://localhost:3000/` using the default credentials (`admin` for both username and password) to access the visual interface, where you can create graphs and track votes in real time.
