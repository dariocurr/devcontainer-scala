# Scala Dev Container

Development environment for Scala projects. Container uses `hseeberger/scala-sbt:11.0.14.1_1.6.2_2.12.15` with user `scala`.

## Use

Install Docker and Visual Studio Code with [Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) support.

1. Clone repository.
2. Open repository in VS Code.
3. Run **Dev Containers: Reopen in Container**.

GitHub Codespaces also detects `.devcontainer/devcontainer.json` automatically.

## Validation

GitHub Actions validates Dockerfile changes pushed to `dev` and pull requests targeting `main`.
