
Like any other tool, notebooks are good for some purposes but bad for some other.

They are good at coding to test out an idea, quick data exploration and visualization, and maybe build out some ML models too.
However, they are bad at modularization (reusability), testability, reproducability, versioning and collaboration. 

Your notebook code does not specify versions (of libraries imported), have hard-coded paths, and untested logic. For your code to be production-ready, it must be versioned, 
reproducible, organised, and tested. 

Steps to be followed for the aformentioned:

1) Create a setup.py file (packaging your code)
2) Create a txt file of requirements (library versions) (using pip freeze in the environment)
3) Add unit test py files
   
4) Prepare code for deployment using container - create Dockerfile (whole environment is declared).
   The Dockerfile builds images into a container that can be run in a laptop, server, cloud. With docker build command, this Dockerfile is built (you may label your container
   with a tag for later use). Using the docker run commmand, you run the container in a laptop, server, or cloud platform.

For ready reference, refer to the repo: https://github.com/datamindedbe/webinar-containers/tree/main/PART%20I




