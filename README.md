# Instructions for building and running OT-Attack container

1. Download repository files
   ```git clone https://github.com/kiddcutty/ot-attack.git```
2. Build container
   ```docker build -f Dockerfile.otattack -t ot-attack .```
3. Run container
   ```docker run --name ot-attack -d --rm --cap-add=NET_ADMIN --privileged --network main ot-attack```
4. Enter container
   ```docker exec -it ot-attack /bin/bash```

**Ensure that the build command is run in the same directory that the ```Exploits``` directory exists.**

## To run NCREPT Modbuster 
On host machine run
```sudo modprobe nfnetlink queue```  

On OT-Attack container run
```iptables -A FORWARD -j NFQUEUE -queue-num 1```
