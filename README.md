# Docker-lamp
Docker lamp PHP / Mysql / Phpmyadmin

PHP 8.1 
- imagick
- pdo_mysql
- pdo_sqlite
- bcmath
- mysqli
- curl 
- zip
- mbstring
- gettext
- calendar
- exif
- soap
- Freetype


# shell
git clone https://github.com/Peterbins/Docker-lamp/.git
cd docker-compose-lamp/
git fetch --all
git checkout 7.4.x
cp sample.env .env
docker-compose up -d
