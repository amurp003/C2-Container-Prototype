# C2-Container-Study
Repository for experimenting with container technologies

## Getting Started using a Docker Container

1. Install and initialize Docker

2. Clone the repository from GitHub into a project-directory; e.g. c2-container-study

#### Fresh Install

        git clone https://github.com/amurp003/c2-container-study.git

#### Re-install with Discard Changes

        cd project-directory
        git status
        git reset --hard
        git pull --rebase

3. We'll use Docker Compose to automatically build and run our containers. However, manual build instructions are included below. 

Ensure that docker compose is installed on the host machine. Navigate the to project main directory and run Docker Compose

        cd project-directory
        docker-compose up -d

## The following named container endpoints should now be available

dss-ui:         http://localhost:5001  
tm-server:      http://localhost:3200/docs  
wa-app:         http://localhost:3201/docs  
te-app:         http://localhost:3202/docs   
opensky-int:    http://localhost:3203/docs  
test-app:       http://localhost:5150/docs 
  
telem-jaeger:   http://localhost:16686  
grafana:        http://localhost:3000  
notebook:       http://localhost:10000

## Stop all containers

        docker stop $(docker ps -a -q)


