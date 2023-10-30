# XEVO Space Game Simulator

Welcome to the XEVO Space Game Simulator! Follow the instructions below to set up and run the project on your Windows machine.

[![Demo Here](https://img.shields.io/badge/-Demo%20Here-blue?style=for-the-badge)](http://xevo.space)
The demo is on Azure.

## Table of Contents
- [Setup on Windows](#setup-on-windows)
- [Setup on Ubuntu](#setup-on-ubuntu)


## Setup on Windows 

### 1. **Install Docker Desktop**
   - Download and install Docker Desktop from [Docker Official Site](https://www.docker.com/products/docker-desktop).
   - Ensure Kubernetes is enabled within the Docker Desktop settings.

### 2. **Clone the Main Repository**
   - Clone the main project repository to a suitable location on your computer.
     ```bash
     git clone https://github.com/tas1337/xevo-kubernetes/
     # or using GitHub CLI
     gh repo clone tas1337/xevo-kubernetes
     ```
   
### 3. **Clone the Sub-Repositories**
   - Navigate inside the `xevo-kubernetes` folder and clone the following repositories.

     #### - **Angular App (The Game)**
       ```bash
       git clone https://github.com/tas1337/xevo-game
       # or using GitHub CLI
       gh repo clone tas1337/xevo-game
       ```
     
     #### - **C++ TLC Server**
       ```bash
       git clone https://github.com/tas1337/xevo-cpp-server
       # or using GitHub CLI
       gh repo clone tas1337/xevo-cpp-server
       ```
     
     #### - **NodeJS HTTP Server**
       ```bash
       git clone https://github.com/tas1337/xevo-api
       # or using GitHub CLI
       gh repo clone tas1337/xevo-api
       ```
   
### 4. **Build and Run the Project**
   - Navigate back to the parent folder (`xevo-kubernetes`).
   - Choose one of the following methods to build and run the project:
   
     #### - **Using Kubernetes**
       ```bash
       kubectl apply -f kubernetes.yaml
       ```
     
     #### - **Using Docker-Compose**
       - Build and run using the repositories you’ve cloned.
         ```bash
         docker-compose up --build
         ```

## Setup on Ubuntu 

#### 1. **Install Docker and Kubernetes**
   Follow the instructions to install [Docker](https://docs.docker.com/engine/install/ubuntu/) and [Kubernetes](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/) on Ubuntu.

#### 2. **Clone the Main Repository**
   ```bash
   git clone https://github.com/tas1337/xevo-kubernetes.git
   ```
#### 3. **Clone the Sub-Repositories**
   Navigate inside the `xevo-kubernetes` folder and clone the sub-repositories as described in the Windows section.

#### 4. **Deployment**
   Follow the same deployment steps as described in the Windows section.


## Conclusion
Your XEVO Space Game Simulator should now be up and running. Enjoy exploring space! 🚀

