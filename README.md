## После установки

- Отключить cdrom в списках репозиториев
- Установить sudo (apt install sudo)
- Добавить пользователя в sudo (sudo adduser имя_пользователя sudo)
- Установка шрифтов (sudo apt install ttf-freefont ttf-mscorefonts-installer)
- Установка программ
	* qalculate - калькулятор
	* vlc - видео плеер
	* gparted - менеджер разделов
	* gufw - файрволл
	* whiskermenu
	* gnome-system-tools
	* шрифт Ubuntu
	* тема Mint-Y
	* иконки Mint-Y
	* curl
	* Heroku CLI
		sudo wget -q — https://toolbelt.heroku.com/install-ubuntu.sh
		chmod +x install-ubuntu.sh
		sudo ./install-ubuntu.sh


## Необходимые программы

- Sublime text
- QBittorrent
- Telegram
- Git
- Foxit reader
- pip
- pip3
- apt install python-virtualenv (virtualenv -p python3 venv)



## Добавление новых репозиториев

sudo nano /etc/apt/sources.list
Добавить contrib non-free в /etc/apt/sources.list

## Настройка Git

- git config --global user.email "you@example.com"
- git config --global user.name "Ваше Имя"
- git config credential.helper store (хранить логин и пароль постоянно)

