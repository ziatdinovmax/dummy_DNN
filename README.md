# dummy_DNN
## Running the notebook via Docker container

Prerequisites:
1. Git client. Usually pre-installed on Linux/Mac, but may need to be installed separately on your Windows OS. See the instructions here: https://git-scm.com/downloads
2. Docker. Installation instructions for Windows, Mac, and Linux can be found here: https://docs.docker.com/get-docker/.

## Build and run docker container
Open the terminal and clone the repository to your local machine:

```git clone https://github.com/tommycwong/dummy_DNN.git```

Then, from your terminal, cd into the cloned repository

```cd dummy_DNN```

and run the following command to build a docker image

```docker build -t dummydnn .```

(you may substitute 'dummydnn' with any name that you like). Use ```--no-cache=true``` before ```-t``` to stop Docker from using cached files. Once it finishes buiding a Docker image, run

```docker run -it --init -p 8080:8080 -v "$(pwd):/home" dummydnn /bin/bash```

to start a container. You will now be able to launch a Jupyter notebook from inside your container by running

```jupyter lab --ip=0.0.0.0 --port=8080 --allow-root```

and follow the on-screen instructions or copy the token number, open http://localhost:8080/ in your browser and enter the copied token.
