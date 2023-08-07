## GitHub Workflows for Docker Projects

This repository contains workflows for Docker Projects.

### **1. GCP Artifact Registry - Docker Build and Push Workflow**

#### Purpose:
This workflow facilitates the building of Docker images and their subsequent push to Google Cloud Platform's Artifact Registry. 

#### Key Components:
- **GCP Artifact Registry Docker Login**: Ensures secure login to GCP's Artifact Registry.
- **Build & Push Docker Image**: Creates a Docker image from the source and pushes it to the specified GCP Artifact Registry repository.

#### Workflow Details:
- **Name**: Docker Build and Push
- **Description**: Builds & Pushes a Docker Image to Docker Repo on GCP Artifact Registry
- **Inputs**:
  - `PLANTON_CLOUD_ARTIFACT_STORE_ID`: ID of the Artifact Store on Planton Cloud.
  - `DOCKER_REPO_HOSTNAME`: Hostname of the Docker repository.
  - `CONTAINER_IMAGE_REPO`: Repository of the Docker image to be built and pushed.
  - `CONTAINER_IMAGE_TAG`: Tag of the Docker image to be built and pushed.

### **Future Workflows**:

1. **AWS ECR - Docker Build and Push Workflow**: 
   This workflow will be responsible for building Docker images and pushing them to the Amazon Web Services' Elastic Container Registry (ECR).

2. **Kubernetes Deployment Workflow**:
   Once Docker images are built and stored, this workflow will automate the deployment of the Docker image as a microservice on a Kubernetes cluster.

### **Usage Notes**:
- Ensure that all required secrets and configurations for authentication are set up in your GitHub repository, especially when interacting with external platforms like GCP.

## Support

If you encounter any issues or require further assistance, please file an issue in this GitHub repository.

## Contributing

If you have suggestions for how this GitHub Action could be improved, or want to report a bug, open an issue! We'd love all and any contributions.

## License

This project is licensed under the [MIT License](LICENSE).
  
