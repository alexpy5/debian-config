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
	* htop
	* aptitude
	* apt-transport-https
	* w64codecs
	* install ntfs-3g ntfs-config
	* unrar
	* secure-delete
		после установки доступны:
	    sfill — для очистки от следов удаленных данных свободного места
	    srm — для надёжного удаления файлов и директорий
	    smem — для очистки оперативной памяти
	    sswap — для очистки раздела подкачки (свопа)
	* dnsutils (nslookup)



## Необходимые программы

- Sublime text
- QBittorrent
- Telegram
- Git
- qpdfview
- pip
- pip3
- Viewnior (просмоторщик изображений)
- apt install python-virtualenv (virtualenv -p python3 venv)



## Добавление новых репозиториев

sudo nano /etc/apt/sources.list
Добавить contrib non-free в /etc/apt/sources.list

## Стандартный sources.list Debian 10

deb https://deb.debian.org/debian buster main contrib non-free
deb-src https://deb.debian.org/debian buster main contrib non-free

deb https://deb.debian.org/debian-security/ buster/updates main contrib non-free
deb-src https://deb.debian.org/debian-security/ buster/updates main contrib non-free

deb https://deb.debian.org/debian buster-updates main contrib non-free
deb-src https://deb.debian.org/debian buster-updates main contrib non-free

## Работа с apt

apt update - обновить список пакетов
apt list --upgradage посмотреть какие пакеты требуют обновления
apt upgrade - обновить систему
sudo apt-get dist-upgrade - когда не обновляются некоторые пакеты

aptitude update
aptitude safe-upgrade

## Настройка автоматического обновления

aptitude update -y && aptitude install unattended-upgrades apt-listchanges -y

Открыть /etc/apt/apt.conf.d/50unattended-upgrades, ниже блока Unattended-Upgrade :: Origins-Pattern добавить:
Unattended-Upgrade::Mail "root";

dpkg-reconfigure -plow unattended-upgrades - выбрать "Да"

Убедиться что в etc/apt/apt.conf.d/20auto-upgrades: 
APT::Periodic::Update-Package-Lists "1";
APT::Periodic::Unattended-Upgrade "1";
И добавить эту строку APT::Periodic::Verbose "2";

В /etc/apt/listchanges.conf проверить: email_address=root


## Настройка Git

- git config --global user.email "you@example.com"
- git config --global user.name "Ваше Имя"
- git config credential.helper store (хранить логин и пароль постоянно)

