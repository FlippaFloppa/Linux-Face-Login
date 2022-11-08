# Facial-Recognition-PAM
Progetto di Sistemi Digitali per Ingegneria Informatica Magistrale Unibo.

## Installing

Build Dockerfile

`sudo docker build . -t debian-pam:test`

Run docker image (**1234** host : **22** container)

`sudo docker run -p 1234:22 -it -d --name PAM debian-pam:test`

Entrare dentro il container con
 
`sudo docker exec -it PAM /bin/bash`
 
Oppure usare l'installer

`chmod +x install.sh && ./install.sh`

## Testing

Provare a loggare con il comando
 
`login`
 
Inserire come username "test" e seguire le istruzioni per bypassare la password
 
Se l'accesso viene eseguito il modulo PAM è utilizzato correttamente

## Abstract
Il progetto si basa su PAM (Pluggable Authentication Module), ovvero un sistema a moduli che è alla base dell’ autenticazione nei moderni sistemi Linux.
PAM è unito al processamento delle immagini ottenute da un flusso di dati registrati da una webcam.
Gli utenti si registreranno con la propria faccia allenando una rete neurale che andrà a costruire un modello da seguire per lo sblocco facciale. Una volta riconosciuti gli utenti tramite la webcam, il sistema si occuperà di effettuare il login.
Il progetto è sviluppato su Raspberry Pi tramite un modulo webcam, che si occuperà di trasferire le informazioni video al Raspberry, ma può essere esteso a una implementazione su webcam integrata in un qualunque sistema Linux. 
Per la nostra implementazione useremo un Raspberry Pi 3, come sistema operativo Debian GNU/Linux 11 (bullseye) ARM e un modulo webcam che si inserisce con un connettore al Raspberry tramite un cavo piatto flessibile.

### Documentazioni PAM:
https://github.com/devinaconley/pam-facial-auth

https://github.com/beatgammit/simple-pam

https://ben.akrin.com/2-factor-authentication-writing-pam-modules-for-ubuntu/

https://wiki.archlinux.org/title/PAM

### Documentazioni OpenCV
https://realpython.com/face-recognition-with-python/

https://pysource.com/2021/08/16/face-recognition-in-real-time-with-opencv-and-python/


