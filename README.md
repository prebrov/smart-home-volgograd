Инструкция предполагает что установлен git:
`sudo apt install git`

Естественно, docker и docker-compose тоже должны быть установлены.

# Запускаем deConz и Home Assistant в docker-compose

1. Склонировать репозиторий в директорию smart-home:
`git clone https://github.com/prebrov/smart-home-volgograd.git smart-home`

2. Перейти в директорию репозитория:
`cd smart-home`

3. Отредактировать файл .env. Заменить в нём пароль в DECONZ_VNC_PASSWORD=set-your-password-here на свой.

4. Собрать контейнеры и запустить их:
`docker-compose up -d`

# Что делать если обновилась эта инструкция

1. Перейти в директорию репозитория:
`cd smart-home`

2. Обновить локальную версию инструкции и конфигурации
`git pull`

# Как обновить deConz и Home Assistant (сам софт внутри контейнеров)

1. Перейти в директорию репозитория:
`cd smart-home`

2. Обновить образы контейнеров:
`docker-compose pull`

3. Пересобрать и перезапустить те контейнеры которые обновились:
`docker-compose up -d`

Никакие данные при этом не должны потеряться.

# Разное

Чтобы рестартануть deConz:
`docker-compose restart deconz`

Чтобы рестартануть Home Assistant:
`docker-compose restart homeassistant`

