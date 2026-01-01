# datalab

The research arm of the Foundation. This is where we bridge urban plans, mathematical climate impact modeling, and urban policy.

### Development Environment Setup

We use a "Twin-Repo" architecture. **datalab** acts as the experimental environment where we draft new planning blueprints with climate models (proxy, while **zzproxies** acts as the production-grade library for leverage them in practice!


#### 1. Prerequisites
* [Docker Desktop](https://www.docker.com/products/docker-desktop/)
* [VS Code](https://code.visualstudio.com/) with the **Dev Containers** extension installed.

#### 2. Local Directory Structure
For the automated environment to work, both repositories must sit in the same parent directory on your machine:
```text
/my-climate-proxy-development/
├── zzproxies/  # git clone https://github.com/zzproxies/zzproxies.git
└── datalab/    # git clone https://github.com/zzproxies/datalab.git (<- Open this in VS Code)
```
  
#### 3. Launching the Environment

Open the **datalab** folder in VS Code & reopen in container.

The build process will:  
    - Construct a Python 3.12.3 environment with needed libraries (see Dockerfile).  
    - Live-mount the zzproxies folder from your laptop into the container.  
    - Install zzproxies in Editable Mode (pip install -e).  


_For Contribution Code of Conduct read CONTRIBUTE.md_
