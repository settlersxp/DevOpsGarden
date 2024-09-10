In order to run this example, you need to have Docker installed on your machine and run the following commands:

Note: The species of the tree is the name of the image tag, here it is Oak. 

```docker build --build-arg species=Oak --build-arg number_of_branches=5 -t Oak .```

To run the Oak container use:

```docker run Oak```

To stop the Oak container use:

```docker stop Oak```

To remove the Oak container use:

```docker rm Oak```

To auto-remove the container once it is exited use:

```docker run --rm Oak```

Refer to the official documentation for more commands and options.
