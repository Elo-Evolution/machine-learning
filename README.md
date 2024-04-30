# Machine Learning
## Getting Started
### Building the Docker Image
Run the following command in the terminal from the root directory of the project to build the Docker image:
<pre>
docker build -t strike-force-ml .
</pre>
This command builds a Docker image named csc468-backend based on the instructions in the Dockerfile.

### Running the Docker Container
After building the image, run the following command to start the container:
<pre>
docker run --name ml-strike-force-service -p 3001:3001 --network my-app-network strike-force-ml
</pre>
This will start the Flask application within a Docker container, applying the environment variables from your .env file and making the app accessible at http://localhost:5000.

## Docker 
You can easily deploy this by pulling the image and building it from docker hub.
<pre>
docker pull maxwellmendenhall/strike-force-ml
</pre>

## Using the /accept_data route
To use this route you need JSON data to POST to it, the JSON data needs to contain 2 keys. They are 'Attacker' and 'Defender'.
