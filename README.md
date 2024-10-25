# Innovation Days - Demo Docker image build and maintenance By Rigoberto Torres

Our purpose is to show the essential configs and best practices for the construction and maintenance of a Docker image.

Key features and best practices implemented:

- Multi-stage build to minimize final image size
- Uses specific Node.js smaller base images and also replicable
- Proper caching of npm dependencies using mount cache

Nginx configuration with:

- Gzip compression
- Security headers
- Proper caching strategies
- SPA routing support
- Static asset optimization

Docker best practices:

- Proper layer caching
- Security considerations
- Healthcheck implementation
- Minimal final image
- Proper file exclusions via .dockerignore

```sh
# Build the image
sudo docker build -t innovation-days:0001 .

# Inspect the image
sudo docker inspect image innovation-days:0001

# Run the container
sudo docker run --name container_innovation_days -d -p 5173:5173 --cpus=2 -m 2048m innovation-days:0001

# Inspect live logs
sudo docker logs -f container_innovation_days

```
