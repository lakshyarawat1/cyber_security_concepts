# Docker Security
## Docker Security Best Practices

### 1. Use Unprivileged Users

- By default, whenever a new container is created, the user is the root user of the container.

- As root user has all the permissions, this may lead to container hijacking and escape too.

- So, it is recommended to run the container as an unprivileged user.

- The method is :

    - `RUN groupadd -r groupname && useradd -r -g groupname username`

- Then we can use the -u flag in docker command to switch the user to the newly created one.

- Still the root user is available as we have not set the password for the root user, so anyone can access it.

- But we can completely block the root user access.

- Using the command :

    - `RUN chsh -s /usr/sbin/nologin root`

### 2. Prevent Privilege Escalation

- We can prevent privilege escalation using a simple docker flag.

- `--security-opt=no-new-privileges image`

- Using this flag prevents any process or subprocess to gain additional access than the privileges provided initially.

- We can use kernel capabilities using `--cap-add` flag to give some privileges to the user.

- It is recommended that we should first drop all capabilities using `--cap-drop all` and then add them as you need.

- Never run a container in privileged mode.

### 3. Securing file systems from unauthorized changes

- We can use the `--read-only` flag to make the file system read-only.

- This will prevent any unauthorized changes to the file system.

- We can use a temporary file system for giving access to selected directories.

- The command is `--read-only --tmpfs /opt`

- Here only the /opt directory will be open for writing and nothing else.

### 4. Disable Inter-container communication

- By default, all the containers can communicate with each other.

- This can be a security risk as one container can access the data of another container.

- We can disable ICC using the command `docker network create --driver brigde -o "com.docker.network.bridge.enable_icc=false"  network-name`


### 5. Do not expose the docker daemon socket 

- The docker daemon socket is used to communicate with the docker daemon.

- If this socket is exposed, then anyone can access the docker daemon and can run any command.

- By default, the socket is run on root that can lead to full control over the container.

- The socket is at `/var/run/docker.sock`

- We can use the command `docker run -v /var/run/docker.sock:/var/run/docker.sock` to access the socket.

- So, it is recommended to not expose the socket.

### 6. Limit resources

- Best way to prevent DoS attack is to limit the resources for the containers.

- We can use the `--memory` flag to limit the memory usage.

- We can use the `--cpus` flag to limit the CPU usage.

- Maxumum number of restarts by `--restart=on-failure:<number>`

- Maximum number of file descriptors by `-ulimit nofile=number`

