# XEVO Space Game Simulator

Welcome to the XEVO Project! This guide provides detailed instructions for setting up and running the project on your local machine. You have the flexibility to use either Kubernetes or Docker-compose for local deployment. This project is entirely open-source, and I've utilized ChatGPT for refactoring and tweaking, as well as GitHub Copilot while building it. I built this project from scratch in just one weekend. I thought it would be really cool to have a TCP server (kind of what WoW uses) that also communicates with a HTTP socket server that can then communicate with a web page in real time. There will also soon be an Unreal Engine 5 demo connected to the TCP server, enabling synchronized movement: when you move in the browser, it's mirrored in the Unreal environment, and vice versa.

###Below is a browser demo, its running on Azure:

<a href="https://xevo.space" target="_blank">
    <img src="https://img.shields.io/badge/-Demo%20Here-blue?style=for-the-badge" alt="Demo Here">
</a>

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
     ```
     # or using GitHub CLI
     ```bash
     gh repo clone tas1337/xevo-kubernetes
     ```
   
### 3. **Clone the Sub-Repositories**
   - Navigate inside the `xevo-kubernetes` folder and clone the following repositories.

     #### - **Angular App (The Game)**
       ```bash
       git clone https://github.com/tas1337/xevo-game
        ```
       # or using GitHub CLI
       
        ```bash
           gh repo clone tas1337/xevo-game
       ```
     
     #### - **C++ TCP Server**
       ```bash
       git clone https://github.com/tas1337/xevo-cpp-server
       ```
       
       # or using GitHub CLI
       ```bash
       gh repo clone tas1337/xevo-cpp-server
       ```
     
     #### - **NodeJS HTTP Server**
       ```bash
       git clone https://github.com/tas1337/xevo-api
       ```
       # or using GitHub CLI
      ```bash
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
   - [### 4. **Build and Run the Project**](#setup-on-ubuntu)


## Conclusion
Your XEVO Space Game Simulator should now be up and running. Enjoy exploring space! 🚀

