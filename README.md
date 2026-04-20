### Keyboard

Немного изменённая тема для виртуальной клавиатуры matchbox-keyboard.

### Macros



### NativeCAM

NativeCAM, в прошлом LinuxCNC Features, <br />
это набор шаблонных программ для создания Gкода обработки прямо на стойке. <br />
Доступны "мастера" для фрезерной, токарной обработки и плазменной резки. <br />

### PyNGCGUI

Создание простых программ обработки для токарного и фрезерного станка.

### Начинающему для LinuxCNC

Автоматический Вход <br />
sudo geany /etc/lightdm/lightdm.conf <br />
sudo mousepad /etc/lightdm/lightdm.conf <br />
autologin-user=ваше имя пользователя <br />

Изолирование Ядра <br />
sudo geany /etc/default/grub <br />
sudo mousepad /etc/default/grub <br />
GRUB_CMDLINE_LINUX_DEFAULT="quiet isolcpus=3" <br />
Обновить загрузчик <br />
sudo update-grub <br />

Добавление архивных репозиториев <br />
sudo geany /etc/apt/sources.list <br />
sudo mousepad /etc/apt/sources.list <br />
Debian 10 buster <br />
deb http://archive.debian.org/debian buster main contrib non-free <br />
deb http://archive.debian.org/debian buster-updates main contrib non-free <br />
deb http://archive.debian.org/debian-security buster/updates main contrib non-free <br />
не обезательно <br />
deb http://archive.debian.org/debian buster-backports main contrib non-free <br />
deb http://archive.debian.org/debian buster-proposed-updates main contrib non-free <br />
