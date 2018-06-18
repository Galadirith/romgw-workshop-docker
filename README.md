# Docker for Workshop on Reduced Order Gravitational-Wave Modeling

This repository contains the Dockerfile for a Docker image that exposes an
environment for Workshop on Reduced Order Gravitational-Wave Modeling.

## Installation

1. **Install Docker**  
   Go to https://www.docker.com/community-edition and follow the instructions
   for your operating system to install Docker. During this process you will be
   prompted to create a Docker account. You will not be able to download and
   install Docker without creating a Docker account.

2. **Pull the Docker image**

   Once you have install Docker and have started Docker on your computer you
   can download the Docker image that contains the ROMGW workshop environment
   with the following command

   ```bash
   docker pull galadirith/romgw
   ```

## Usage

1. **Download ROMGW files**  
   Download the files for the workshop.

2. **Start Jupyter notebook or a lab**  

    To use Jupyter lab run

   ```bash
   docker run --rm -it -v <path-to-romgw-workshop-folder>:/download -w /download -p 8888:8888 --name lab -h localhost galadirith/romgw jupyter lab --allow-root --ip=0.0.0.0
   ```

   or to use the normal Jupyter notebook interface run

   ```bash
   docker run --rm -it -v <path-to-romgw-workshop-folder>:/download -w /download -p 8888:8888 --name lab -h localhost galadirith/romgw jupyter notebook --allow-root --ip=0.0.0.0
   ```

3. **Open Jupyter in your browser**  
   Copy the link that gets displayed in your terminal window to a browser
   window.

## License

`rowgw-workshop-docker` is released under the [MIT license](LICENSE.md).
