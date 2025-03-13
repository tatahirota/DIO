version: '3.8'   
services:   
  apache:   
    image: httpd:latest   
    container_name: apache-desafio1-web-dio   
    ports:   
      - '80:80'  
    volumes:
      - ./site-desafio:/usr/local/apache2/htdocs/   
      
    networks:   
      - minha-net   
     
networks:   
    minha-net:      
      driver: bridge      

   
##################################################
################### COMANDOS #####################
##################################################

#1- CRIAR PASTA DO PROJETO
#mkdir meu-projeto-dio

#2- ENTRAR NA PASTA DO PROJETO
#cd meu-projeto-dio

#3- CRIAR PASTA DO SITE DENTRO DA PASTA DO PROJETO
#mkdir site-desafio

#4- CRIAR O COMPOSE COM O CÓDIGO CITADO INICIALMENTE (NA MESMA PASTA)
#sudo nano docker-compose.yml

#5- CRIAR O ARQUIVO HTML (NA MESMA PASTA)
#sudo nano index.html
#<!DOCTYPE html>
#<html lang="pt-br">
#<head>
#<meta charset="UTF-8">
#<meta name="viewport" content="width=device-width, initial-scale=1.0">
#<title>Meu Site Apache</title>
#</head>
#<body>
#<h1>Olá, Mundo! Este é meu site para o desafio da DIO de Docker com Apache!</h1>
#</body>
#</html>


#6- INSTALAR O COMPOSE NO CONTAINER (CASO NAO TENHA)
#apt install docker-compose

#7- INICIAR O DOCKER-COMPOSE.YML QUE ESTÁ NA PASTA DO PROJETO
#docker-compose up -d

#8- ABRIR O NAVEGADOR E DIGITAR:
#http://localhost
# http://localhost
