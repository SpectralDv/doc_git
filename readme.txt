git init
(.gitignore = [.gitignore .vscode/*])
git add .
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SpectralDv/....git
git push -u origin main

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
3.5.add new branch
git checkout -b mybranch
3.6.Upload to git
git branch -M 'main'
git push -u origin 'main'

4.Принудительный push
git push --force

5.Принудительный pull
git fetch --all
git reset --hard origin/main

sudo nano /etc/ssh/sshd_config
sudo service ssh restart

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



sudo snap install --classic code


sudo apt-get install libpcap0.8-dev  
sudo apt-get install pcap*
sudo apt-get install libpcap-dev


1.Создайте файл toolchain.cmake: Создайте файл toolchain.cmake в корне проекта с содержимым, соответствующим вашей платформе. Например, для Raspberry Pi 4:
set(CMAKE_SYSTEM_NAME Linux)
set(CMAKE_SYSTEM_PROCESSOR arm)
set(CMAKE_C_COMPILER /usr/bin/arm-linux-gnueabihf-gcc)
set(CMAKE_CXX_COMPILER /usr/bin/arm-linux-gnueabihf-g++)

1.2.Для Radxa Zero 3W:
set(CMAKE_SYSTEM_NAME Linux)
set(CMAKE_SYSTEM_PROCESSOR aarch64)
set(CMAKE_C_COMPILER /usr/bin/aarch64-linux-gnu-gcc)
set(CMAKE_CXX_COMPILER /usr/bin/aarch64-linux-gnu-g++)

2.Создайте каталог для сборки:
mkdir build
cd build

3.Настройте сборку с помощью CMake:
cmake -DCMAKE_TOOLCHAIN_FILE=../toolchain.cmake ..

4.Теперь, когда вы настроили CMake, вы можете скомпилировать проект:
make -j$(nproc)

5.После успешной компиляции вы получите исполняемые файлы, которые можно перенести на ваше устройство Raspberry Pi 4 или Radxa Zero 3W. Используйте scp или rsync для копирования файлов на устройство:
scp your_executable pi@<raspberry_pi_ip>:/path/to/destination

