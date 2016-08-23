# Node-React-Webpack

This is an early, barebones dev framework to create Node.js applications with React.

## Installing

Git clone the repo:

    $ git clone https://github.com/da-n/node-react-webpack

Install and configure [Docker](https://www.docker.com/), it should only take a few minutes. Now we can run the following Docker commands from the projects root folder to build the image and container:

    $ docker build --build-arg MODE=dev -t "node-react-webpack" .
    $ docker run -p 3000:3000 -v $HOME/path/to/repo/:/usr/src/app/ -d node-react-webpack

*Note by default the Dockerfile is set to build images in production mode, the above command will instead run it in `dev` mode. Remove `--build-arf MODE=dev` to instead run in production mode.*

Once the container is up and running, you can exec into it to run commands with the following where `container_name` is the name given to your docker container:

    $ docker exec -it container_name /bin/bash

You can see the name of the container by running the following command:

    $ docker ps -a

You should be able to see the server running at [http://localhost:3000](http://localhost:3000).

##

## License

Node-React-Webpack is released under the MIT license. See [LICENSE](LICENSE) for details.
