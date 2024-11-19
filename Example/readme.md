
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

For ready reference, refer the repo: https://github.com/datamindedbe/webinar-containers/tree/main/PART%20I

Next comes portability - how about the container running in environments other than the one I built and ran successfully. 

Checking whether (Docker) container works everywhere? Shipping container to the cloud AWS is the use case.

Main ingredients for container runtime:
1. **Build**: We need to use a tool to let us declare what we need in the container to run our application. **Buildkit** is probably the most well-known, also used by docker.
2. **Store**: we need a place to host the images so our runtime will be able to fetch the images and run them as containers. This is typically called a container registry. **Docker Hub** is by and large the most popular for this. Other examples are AWS Elastic Container Registry (ECR), Azure Container Registry (ACR), Google Container Registry.
3. **Run**: we need a container runtime to let us run our freshly built images. **containerd** is probably the most used runtime.

   If you're running multiple containers, Kubernetes is the one.

   Output post running container:
   1. **Logs**: configured the container definition to store the logs on AWS Cloudwatch
   2. **Results**: configured the container to read and write to a specific AWS S3 bucket, and going there we can have a look at the csv file (of predictions) that was produced.

   For details, please see: https://github.com/datamindedbe/webinar-containers/tree/main/PART%20II

   Reference repo: https://github.com/datamindedbe/webinar-containers
   

   








