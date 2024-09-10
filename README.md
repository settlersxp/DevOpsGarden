# DevOpsGarden
Use a garden example to showcase devops technologies.


## Introduction 
    In the Docker directory there is an example of a multistep docker recipe which on build time creates a tree based 
on the environment variables such as "species" and "number_of_branches". The values of these variables are passed
to the docker build command. The tree is created in the /tmp directory and the tree is printed to the console.

    In the DockerCompose directory there is an example of a docker-compose file which creates multiple trees with different
species and number of branches. The values of these variables are passed to the docker-compose up command. 
Each tree type is separated from the others based on the network it belongs to.