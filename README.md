How it works:
- We set our public key using env variable
- In Dockerfile for container1 we write public key to authorized_keys
- In Dockerfile for container1 we create user docker_root and generate ssh keys for this user
- Using ansible creating container1 and using ansible shell getting generated public key
- Using ansible set this key as a env variable
- In Dockerfile for container2 we create docker_root user and add docker_root user generated pub key to authorized_keys
- Using ansible creating container2, link it to container1
- Using ansible check connectivity between two containers

