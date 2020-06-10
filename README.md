# Запускаем deConz в docker-compose

1. Убедиться что стоит git, поставить его, если не стоит:
`sudo apt install git`

2. Склонировать репозиторий в директорию smart-home:
`git clone https://github.com/prebrov/smart-home-volgograd.git smart-home`

3. Перейти в директорию репозитория:
`cd smart-home`

4. Отредактировать файл .env. Заменить в нём пароль в DECONZ_VNC_PASSWORD=set-your-password-here на свой.

5. Запустить docker-compose:
`docker-compose up -d`

Чтобы рестартануть deConz:
`docker-compose restart deconz`