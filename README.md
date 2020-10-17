# dummy_DNN
First, clone the repository to your local machine. Then, from your terminal, cd into the cloned repository and run

```docker build -t dummydnn .```

(you may substitute 'dummydnn' with any name that you like). Use ```--no-cache=true``` before ```-t``` to stop Docker from using cached files. Once it finishes buiding a Docker image, run

```docker run -it --init -p 8080:8080 -v "$(pwd):/home" dummydnn /bin/bash```

to start a container. You will now be able to launch a Jupyter notebook from inside your container by running

```jupyter lab --ip=0.0.0.0 --port=8080 --allow-root```

and follow the on-screen instructions or copy the token number, open http://localhost:8080/ in your browser and enter the copied token.
