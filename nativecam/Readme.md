### NativeCAM

NativeCAM, в прошлом LinuxCNC Features, <br />
это набор шаблонных программ для создания Gкода обработки прямо на стойке. <br />
Доступны "мастера" для фрезерной, токарной обработки и плазменной резки. <br />

### Установка:
Устанавливаем nativecam_0.1.14b_all.deb <br />
с помощью программы установки пакетов gdebi. <br />
Если gdebi не установлен в системе то установите <br />
его спомощью менеджера пакетов Synaptic. <br />
Установка вручную (не проверял): sudo dpkg -i nativecam_0.1.14b_all.deb <br />
Установить все отсутствующие зависимости: sudo apt --fix-broken install <br />
В терминале выполняем: ncam -h если вылезла помощь значит пакет установился. <br />

### Настройка:
Создаем конфиг своего станка, парпимер с именем Stanok <br />
заходим в терминале в каталог станка: cd ~/linuxcnc/configs/Stanok <br />
выполняем: ncam -i Stanok.ini -c lathe <br />
Где lathe может быть plasma или mill смотря что вам надо, <br />
если использовать опцию -t вместо -c он будет встроен во вкладку. <br />
Должно создать бекап ini файла и дописать конфигурацию станка. <br />
Откроется окно мастера, закрываем его и запускаем свой конфиг станка. <br />

### Примеры:
ncam -i Stanok.ini -c mill <br />
ncam -i Stanok.ini -c lathe <br />
ncam -i Stanok.ini -c plasma <br />

ncam -i Stanok.ini -t mill <br />
ncam -i Stanok.ini -t lathe <br />
ncam -i Stanok.ini -t plasma <br />

### Исходники:
https://github.com/FernV/NativeCAM <br />
Поддерживает LinuxCNC до 2.8.4 установка на LinuxCNC 2.9.3 обсуждается тут: <br />
https://forum.linuxcnc.org/nativecam/53492-nativecam-on-linuxcnc-2-9-3?start=0 <br />
