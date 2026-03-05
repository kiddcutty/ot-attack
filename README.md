# Instructions for building and running OT-Attack container

1. Download repository files
   ```git clone ```
2. Build container
   ```docker build -f Dockerfile.otattack```
3. Run container
   ```docker run --name ot-attack -it --rm --cap-add=NET_ADMIN --privileged --net=host ot-attack```

**Ensure that the build command is run in the same directory that the ```Exploits``` directory exists.
