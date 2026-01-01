FROM ghcr.io/osgeo/gdal:ubuntu-small-latest

RUN apt-get update && apt-get install -y \
    python3-pip \
    python3-venv \
    python3-dev \
    libspatialindex-dev \
    git \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash vscode
WORKDIR /workspaces/datalab
RUN chown vscode:vscode /workspaces/datalab

USER vscode
RUN python3 -m venv /home/vscode/venv
ENV PATH="/home/vscode/venv/bin:$PATH"

RUN pip install --upgrade pip