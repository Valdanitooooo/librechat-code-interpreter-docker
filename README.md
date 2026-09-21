# LibreChat Code Interpreter Docker Images

This project automatically builds Docker images for the [LibreChat Code Interpreter](https://github.com/LibreChat-AI/code-interpreter).

Since the upstream project primarily builds from source and does not provide official pre-built images, this project leverages GitHub Actions to automatically track the latest upstream releases, build the corresponding Docker image versions, and publish them to Docker Hub.

## Images

The following 6 images are currently available. The image tags match the upstream releases, for example:


- [valdanito/librechat-code-interpreter-api:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-api/tags)
- [valdanito/librechat-code-interpreter-worker:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-worker/tags)
- [valdanito/librechat-code-interpreter-egress-gateway:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-egress-gateway/tags)
- [valdanito/librechat-code-interpreter-tool-call-server:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-tool-call-server/tags)
- [valdanito/librechat-code-interpreter-sandbox-runner:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-sandbox-runner/tags)
- [valdanito/librechat-code-interpreter-file-server:v1.x.x](https://hub.docker.com/r/valdanito/librechat-code-interpreter-file-server/tags)


This project only builds the latest official releases; it does not build historical versions, nor does it publish a `latest` image.

## Automated Builds

GitHub Actions periodically checks for the latest upstream releases.

When a new release is detected, it automatically fetches the source code from the corresponding tag, builds all images, and pushes them to Docker Hub.
