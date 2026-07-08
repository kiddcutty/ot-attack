# Instructions for building and running OT-Attack container

1. Download repository files
   ```git clone https://github.com/kiddcutty/ot-attack.git```  
2. Navigate to *ot-attack* directory
   ```cd ot-attack/```
3. Build container
   ```docker build -f Dockerfile.otattack -t ot-attack .```
4. Run container
   ```docker run --name ot-attack -d --rm --cap-add=NET_ADMIN --privileged --network host ot-attack```
5. Enter container
   ```docker exec -it ot-attack /bin/bash```

**Ensure that the build command is run in the same directory that the ```Exploits``` directory exists.**

## To run NCREPT Modbuster 
On host machine run
```sudo modprobe nfnetlink queue```  
