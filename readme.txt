1.Clon a repository(making 2.)
git clone https://github.com/... .

2.Include download to the repository 
mkdir /forgit
cd /forgit
git init
git remote add origin https://github.com/...
git pull https://github.com/...
git pull origin main
2.1.For update and remove locale changes
git reset --hard
git pull origin main

3.Залить измеения в репозиторий
3.1.Check files for change to commit
git status
3.2.Add change to commit
git add .
3.3.Check files for change to commit
git status
3.4.Make commit with comment
git commit -m "comment"
git log
3.5.Upload to git
git branch -M 'main'
git push -u origin 'main'

4.Принудительный push
git push --force

5.Принудительный pull
git fetch --all
git reset --hard origin/main

6.Принудительно закрыть сокеты
/etc/init.d/networking restart

7.Монтирование через конфиг
sudo nano /etc/fstab
mount -av
umount /path_local

8.Создание конфига для запуска веб сервера 
sudo nano /etc/supervisor/conf.d/webserver.conf
sudo service supervisor restart

9.Указать домент и порт супервизору
sudo nano /etc/supervisor/supervisord.conf

"<style>body{background-color:#000;}</style>"

server = new
webserver = old

https://blog.sedicomm.com/2018/02/06/kak-ustanovit-i-nastroit-openvpn-server-na-debian-9-za-5-minut/

sudo nano /etc/nginx/sites-available/default
sudo nano /etc/apache2/sites-available/000-default.conf
