Docker compose can also build images, but it is more commonly used to run multiple containers at once.

This is useful when you have multiple services that need to interact with each other.

For the clarity of this example 3 species of tree images will be build manually using the docker build command.
This kind of step, of building images, usually is part of a CI/CD pipeline. The pipeline can be a bash script, a Jenkins
job, or a GitHub action etc.

```
docker build --build-arg species=Oak --build-arg number_of_branches=5 -t Oak .
docker build --build-arg species=Pine --build-arg number_of_branches=3 -t Pine .
docker build --build-arg species=Maple --build-arg number_of_branches=7 -t Maple .
```

In order to showcase the usage of environment variables in the docker-compose file, each tree will receive an age as an
environment variable.

The gardener will be able to access the tree networks and act as an entry point in the garden.

As you can see the cluster of trees can be scaled up and can be maintained but there are not that many configurations
that can be done.

Kubernetes is a more advanced tool that can be used to manage containers in a more complex dynamic way.
