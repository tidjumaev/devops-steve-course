# How to install Docker on MacOS - RWieruch

Just recently I had to install Docker on my MacOS machine. Here I want to give you a brief walkthrough on how to achieve it. First of all, we need Homebrew to install all the necessary Docker dependencies. If there isn't a Homebrew installation on your Mac, follow [this guide for a developer setup](https://www.robinwieruch.de/developer-setup).

Install the docker dependency with Homebrew after making sure that all Homebrew dependencies are on the latest version:

```text
brew updatebrew install docker
```

You will also need a **MacOS specific environment** in which Docker can be used, because natively Docker uses a Linux environment. Therefore, install the docker-machine and virtualbox dependencies:

```text
brew install docker-machinebrew cask install virtualbox
```

Note: If the last install fails, check your MacOS' System Preference and verify if _System software from developer "Oracle America, inc" was blocked from loading._ shows up. If you see it, hit the "Allow"-button and install it again.

Optional: if you want to use **Docker Compose** later, install the docker-compose dependency with Homebrew:

```text
brew install docker-compose
```

Everything related to Docker and its environment is installed now. Let's get started with using it. First, **create an engine for Docker on MacOS**. This needs to be done only once, unless you want to create more than one engine by giving them other names than `default`. Usually one engine should be sufficient.

```text
docker-machine create --driver virtualbox default
```

Using the following command for your Docker Machine, you should see whether your last Docker engine got created and whether you have more than one engine if desired:

```text
docker-machine lsNAME      ACTIVE   DRIVER       STATE     URL   SWARM   DOCKER    ERRORSdefault   -        virtualbox   Stopped                 Unknown
```

Usually the Docker engine's `STATE` should be `Running`. If it isn't, like it's shown in the last output, you can start the engine with Docker Machine:

```text
docker-machine start default
```

Checking your **list of Docker engines** again should lead you to one running Docker engine:

```text
docker-machine lsNAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER     ERRORSdefault   -        virtualbox   Running   tcp://192.168.99.100:2376           v19.03.5
```

Just for the sake of knowing about it, you can stop your Docker engine anytime too:

```text
docker-machine stop default
```

Make sure that your Docker engine is running for the next steps. Last, we need to **configure the environment variables for Docker**. Run the following command to find out how:

```text
docker-machine env defaultexport DOCKER_TLS_VERIFY="1"export DOCKER_HOST="tcp://192.168.99.100:2376"export DOCKER_CERT_PATH="/Users/mydspr/.docker/machine/machines/default"export DOCKER_MACHINE_NAME="default"# Run this command to configure your shell:# eval $(docker-machine env default)
```

Usually this prints out the command to set all the env variables set for MacOS; which is the following:

```text

```

Finally, you should be able to start a **Docker container** with a pre-defined **Docker image** to check whether everything works as expected:

```text
docker run hello-worldHello from Docker!This message shows that your installation appears to be working correctly.
```

The first time running this command should take some time, because the pre-defined Docker image is pulled from a remote server. Every additional time you run this command, it should print its output almost in an instant, because the Docker image is already there and the build for the Docker container from the Docker image doesn't take long for this example. Congratulations, Docker is running on your Mac machine now.

