FROM ft-rails:on-build
#crée l'image une image pour le project 
EXPOSE 3000
CMD [ "rails" , "s", "-b", "0.0.0.0", "-p", "3000"]
#CMD est ma command: rails s -b 0.0.0.0 -p 3000
#rails s(pour commencer le serveur rails) b(bind Rails a une adresse specific le default cest localhost -d sera daemon) 0.0.0.0 l'ip puis le port
# How to build it?
# docker build -t ex02 .

# How to run it?
# docker run -it --rm -p 3000:3000 ex02
