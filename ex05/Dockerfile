FROM node:25-alpine3.22

# mapping (local) vscode/ex05 <-> app/api (docker)
WORKDIR /app/api

# declare port to be used by the container
EXPOSE 3000

# command to run when the container starts with docker run -v <local_path>:<container_path> 
# -p <local_port>:<container_port> <image_name> 
CMD ["npm", "run", "start"]