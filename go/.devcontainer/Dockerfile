FROM mcr.microsoft.com/devcontainers/go:1.25-bookworm

WORKDIR /workspace

# Make sure vscode owns the Go cache directories
RUN mkdir -p /home/vscode/go/pkg/mod /home/vscode/.cache/go-build \
    && chown -R vscode:vscode /home/vscode/go /home/vscode/.cache/go-build
