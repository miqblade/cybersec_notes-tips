# Основні команди навігації
pwd                  # показати поточний каталог

ls                   # показати файли (ls -la для прихованих)

cd <каталог>         # перейти в каталог

cd ..                # на рівень вище

cat <файл>           # показати вміст

less <файл>          # посторінковий перегляд

head / tail <файл>   # початок / кінець файлу

touch <файл>         # створити порожній файл

mkdir <каталог>      # створити каталог

rm <файл>            # видалити файл

rmdir <каталог>      # видалити порожній каталог

rm -rf <каталог>     # видалити рекурсивно (обережно!)

cp / mv              # копіювання / переміщення

find / grep          # пошук файлів або тексту

# Система та процеси

top / htop           # моніторинг процесів
ps aux               # список процесів
kill -9 <PID>        # знищити процес
df -h                # стан дисків
du -sh *             # розмір файлів/каталогів
free -h              # пам'ять
uptime               # скільки система працює
uname -a             # інформація про ядро
lscpu / lsblk / lspci / lsusb   # інформація про апаратне забезпечення
dmesg | tail         # системні повідомлення
journalctl -xe       # перегляд логів systemd

# Доступ, права, користувачі

whoami               # поточний користувач
id                   # UID, GID
sudo <команда>       # виконати як root
su                   # змінити користувача
adduser / deluser    # додати / видалити користувача
passwd               # змінити пароль
chmod 755 <файл>     # права доступу
chown user:group <файл> # змінити власника
groups / who / w     # хто в системі

# Мережеві команди

ifconfig / ip a      # мережеві інтерфейси
ping <адреса>        # перевірити зв’язок
traceroute <адреса>  # маршрут до хоста
netstat -tulnp       # відкриті порти (або ss -tulnp)
nmap <ціль>          # скан портів
curl / wget <url>    # завантаження
dig / nslookup       # DNS запити
ssh user@ip          # підключення до сервера
scp <файл> user@ip:/path   # передача файлів

# Робота з пакетами

apt update && apt upgrade   # оновлення системи
apt install <пакет>         # встановити
apt remove <пакет>          # видалити
dpkg -l                    # список встановлених
snap install <пакет>       # альтернативний менеджер


# Архіви та текст

tar -xvf file.tar           # розпакувати
tar -czvf file.tar.gz dir   # запакувати
zip -r file.zip dir         # створити zip
unzip file.zip              # розпакувати
nano / vim <файл>           # редагувати

# Bash / скрипти

echo "текст" > file.txt
cat file.txt | grep "слово"
for f in *.txt; do echo $f; done
chmod +x script.sh
bash script.sh


# Системне управління

systemctl start/stop/status <сервіс>
service <ім’я> restart
crontab -e          # налаштувати автозапуск
shutdown -r now     # перезавантаження
reboot              # теж саме
history             # історія команд
alias ll='ls -la'   # скорочення


# Рекогносцировка (OSINT & DNS)

whois example.com — інформація про домен/реєстранта.
dig +short example.com A — швидко отримати A-запис.
dig @8.8.8.8 example.com ANY — повні DNS-запити через конкретний DNS-сервер.
nslookup example.com — альтернативний DNS-інструмент.
host -a example.com — детальний DNS lookup.


# Сканування мережі / хостів (безпечне виявлення)

nmap -sS -Pn -p- 10.10.10.5 — TCP SYN scan, всі порти, без ping.
nmap -sV -sC -O 10.10.10.0/24 — версії сервісів, скрипти NSE та OS detection по підмережі.
nmap -T4 --min-rate 1000 -p 1-65535 target — швидкий агресивний порт-скан.
masscan -p1-65535 --rate=10000 10.0.0.0/8 — швидке сканування великих мереж.
