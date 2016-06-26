# DockerVI

标签（空格分隔）： Docker

---
![docker][1]
> Project DockerVI is inspired by the idea of realize the Visible Management for **[Docker Swarm][2]** by using Docker Swarm Remote API . The goal is to provide a beauty and power pure client side implementation,  make  it is effortless to connect and manage docker swarm.


### Current implementation features
* **Display the overall survey of cluster**.
* **Container:**
    * show Container list in swarm cluste.
    * Create, Running, Stop, Delete Container.
    * Look up the low-level information on the container.
    * View the real-time resource usage in Container.
    * View the stdout and stderr logs from the Container.
* **Image:**
    * show Image list in swarm cluste.
    * Search, Pull, Delete Image.
    * Create Container using Image.
* **Volume:**
    * show Volume list in swarm cluste.
    * Create, Delete Volume.
    * Search volume by using volume name or host name;
    * Look up the low-level detail information about volume.

### Some Demo
<div align="center">
<img src="http://o9dop9y2w.bkt.clouddn.com/cluster.png" width = "90%" height = "250" alt="cluster" align=center/>
</div>
<div align="center">
<img src="http://o9dop9y2w.bkt.clouddn.com/realTimeResourceState.png" width = "90%" height = "250" alt="Containerstate" align=center/>
</div>
<div align="center">
<img src="http://o9dop9y2w.bkt.clouddn.com/containerCreate.png" width = "90%" height = "250" alt="createContainer" align=center/>
</div>

### Getting Started
DockerVI is self-contained and can be easily deployed via [docker-compose][4](Quick-Start steps below).

**System requirements:**  
DockerVI need works with docker 1.10+ and docker-compose 1.6.0+.

1. Get the source code:

    ```sh
    $ git clone https://github.com/gaoyangxiaozhu/DockerVI.git
    ```
2. Edit the file **Deploy/config.js**, make necessary configuration changes such as hostname for deploy project and swarm address.

3. Install DockerVI with the following commands. Note that the docker-compose process can take a while.
    ```sh
    $ cd Deploy
    $ ./prepare.sh

    $ docker-compose up
    ```

If everything worked properly, you should be able to open a browser to manage your docker swarm using
    `http:<deployed host ip>:8100`



### Stack
* [Angular](https://github.com/angular/angular.js)
* [nodeJs](https://nodejs.org/en/)
* [Express](https://github.com/expressjs/express/)
* [socket.io](https://github.com/socketio/socket.io/)
*  [Bootstrap](http://getbootstrap.com/)
* [Jade](http://jade-lang.com/)
* [Compass](http://compass-style.org/)
* [Docker compose](https://docs.docker.com/compose/overview/)


### Todo:
* Full remote swarm api support
* using websocket technology for into the container in browser to carry out the command operation  
* Unit tests


### License
The UI For Docker code is licensed under the MIT license.


  [1]: http://o9dop9y2w.bkt.clouddn.com/docker.png
  [2]: https://docs.docker.com/engine/swarm/
  [4]: https://docs.docker.com/compose/overview/
