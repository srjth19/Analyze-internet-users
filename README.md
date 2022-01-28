# Run MONGODB from Docker

## Prerequisites:
1. Docker
2. Git
3. Any IDE(optional)

## How to run MongoDB:
1. Run docker daemon on your system.
2. Clone this repo to your local drive.
3. Open terminal(or cmd if you are on Windows) and change current working directory to the repo.
4. Run the command "docker compose up -d" to start the MongoDB and Mongo Express containers.

## Accessing MongoDB:
### Using Shell
1. Use docker ps to check the conatiner ID of MongoDB
2. Run command "docker exec -it <container ID> bash" to access Bash terminal.
3. Once inside bash, run command "mongo mongodb://localhost:27017 -us <username> -p <password>" to access Mongo Shell
You can get the credentials from the docker-compose.yaml document where you define the environmental variables.

### Using Mongo-Express
Go to your browser and connect to "localhost:<port id>" to access Mongo-Express
You can get the port passed to the container from the docker-compose.yaml document.

You can use the mock data provided in the Data folder to test your db and to test any scripts as needed. 