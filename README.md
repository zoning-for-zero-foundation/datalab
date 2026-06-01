# datalab

The research arm of the Foundation. This is where we bridge urban plans, mathematical climate impact modeling, and urban policy.

### Development Environment Setup

We use a "Twin-Repo" architecture. **datalab** acts as the experimental environment where we draft new planning blueprints with climate models, while **zzproxies** acts as the production-grade library for leverage them in practice!


#### 1. Prerequisites
* [Docker Desktop](https://www.docker.com/products/docker-desktop/)
* [VS Code](https://code.visualstudio.com/) with the **Dev Containers** extension installed.

#### 2. Local Directory Structure
For the automated environment to work, both repositories must sit in the same parent directory on your machine:
```text«
/my-climate-proxy-development/
├── zzproxies/  # Clone: https://github.com/zzproxies/zzproxies.git
└── datalab/    # Clone: https://github.com/zzproxies/datalab.git
```

#### 3. Launching the Environment

- Open the **datalab** folder in VS Code & reopen in container.
    The build process will:  
    - Construct a Python environment with needed libraries (see Dockerfile).  
    - Live-mount the zzproxies folder from your laptop into the container.  
    - Install zzproxies in Editable Mode (pip install -e).  
- After build process, from File -> Open workspace from File.." and select "datalab.code-workspace"  

You can now develop on both repositories simultaneously! Your changes in zzproxies will be instantly available in datalab. When you have a new proxy candidate ready, please submit a PR to the zzproxies repository!
