# Zadanie nr 2

ZW tym zadaniu należy zbudować prosty plik docker-compose.yml, który
pozwoli na uruchomienie znanej z innych zajęć, uslugi LEMP wraz z phpMyAdmin. Stack
LEMP składa się z następujących usług składowych: 
---- L – dla Linux; 
---- E – dla Nginx; 
---- M – dla MySQL; 
---- P – dla PHP. 
Wobec tego projekt zawiera cztery kontenery (usługi): 
- jeden kontener dla Nginx; 
- jeden kontener dla PHP (PHP-FPM) https://php-fpm.org/ ; 
- jeden kontener dla MySQL; 
- jeden kontener dla phpMyAdmin. 
Założenia dla uslugi:
- serwery są budowane zgodnie z dokumentacją obrazów bazowych dostępnych na
DockerHub i umieszczonych tam plików Dockerfile.
- serwery PHP, MySQL, phpMyAdmin są przyłączone do sieci backend a Nginx do
backend oraz frontend. Nginx ma wystawiony na świat zewnętrzy port 6666.
- serwer Nginx ma wyświetlać stronę startową php (index.php).
- serwer phpMyAdmin ma być dostępny na porcie 6001 i powinno być możliwe
zalogowanie się do niego i założenie testowej bazy.

## a)
Uruchomienie stacka: `docker compose up -d`.

## b+c)
Uruchomienie phpmyadmin i utworzenie testowej bazy danych: `docker exec zadanie2_mysql_1 mysql --execute="CREATE DATABASE test" --user=root --password=root`.

Plik ilustrujacy strukture projektu: 
![docker-compose.yml](https://github.com/bezqyczekpl/BazaDanych/docker-compose.png?raw=true)
