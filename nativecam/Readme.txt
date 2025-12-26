NativeCAM

NativeCAM, в прошлом LinuxCNC Features,
это набор шаблонных программ для создания Gкода обработки прямо на стойке.
Доступны "мастера" для фрезерной, токарной обработки и плазменной резки.

Установка:

Устанавливаем nativecam_0.1.14b_all.deb
с помощью программы установки пакетов gdebi.
Если gdebi не установлен в системе то установите
его спомощью менеджера пакетов Synaptic.
Установка вручную (не проверял): sudo dpkg -i nativecam_0.1.14b_all.deb
Установить все отсутствующие зависимости: sudo apt --fix-broken install
В терминале выполняем: ncam -h если вылезла помощь значит пакет установился.

Настройка:

Создаем конфиг своего станка, парпимер с именем Stanok
заходим в терминале в каталог станка: cd ~/linuxcnc/configs/Stanok
выполняем: ncam -i Stanok.ini -c lathe
Где lathe может быть plasma или mill смотря что вам надо,
если использовать опцию -t вместо -c он будет встроен во вкладку.
Должно создать бекап ini файла и дописать конфигурацию станка.
Откроется окно мастера, закрываем его и запускаем свой конфиг станка.

Примеры:

ncam -i Stanok.ini -c mill
ncam -i Stanok.ini -c lathe
ncam -i Stanok.ini -c plasma

ncam -i Stanok.ini -t mill
ncam -i Stanok.ini -t lathe
ncam -i Stanok.ini -t plasma

Исходники:

https://github.com/FernV/NativeCAM
Поддерживает LinuxCNC до 2.8.4 установка на LinuxCNC 2.9.3 обсуждается тут:
https://forum.linuxcnc.org/nativecam/53492-nativecam-on-linuxcnc-2-9-3?start=0