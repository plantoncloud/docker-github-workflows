# GitHub Workflow: Docker Build and Push

This repository provides a GitHub Workflow that automates the process of building a Docker image and pushing it to the specified Docker repository using Planton Cloud.

The composite workflow is split into two distinct actions:

1. **Build Docker Image:** This action automates the process of building a Docker image.
2. **Docker Build and Push:** This action automates the entire process of both building the Docker image and pushing it to the specified Docker repository.

The workflow performs the following steps:

1. **Fetch Artifact Store Key:** Retrieves the writer key from Planton Cloud for the artifact store specified.

2. **Docker Login:** Logs into the Docker repository using the fetched writer key.

3. **Docker Build:** Constructs the Docker image from the current directory.

4. **Docker Push:** Uploads the built Docker image to the specified Docker repository.

## Usage

To leverage this composite workflow in your own workflows, reference it in your GitHub Actions. The workflow can be incorporated using the `uses` directive.

```yaml
uses: <path_to_composite_action>@version
```

### Inputs

The composite action requires the following inputs:

- `PLANTON_CLOUD_ARTIFACT_STORE_ID`: ID of the Artifact Store on Planton Cloud.
- `DOCKER_REPO_HOSTNAME`: Hostname of the Docker repository.
- `CONTAINER_IMAGE_REPO`: Repository of the Docker image to be built and pushed.
- `CONTAINER_IMAGE_TAG`: Tag of the Docker image to be built and pushed.

## Contributing

For suggestions or bug reports related to this GitHub Action, please open an issue. Contributions of all forms are appreciated.

## License

This project is under the [MIT License](LICENSE).
