FROM ubuntu

MAINTAINER auguitar

RUN apt-get update && apt-get install -y emacs

CMD ["/usr/bin/emacs", "-f", "tetris"]

#Commande de build: docker build -t tetris .

#Commande de lancement: docker run --rm -ti tetris
