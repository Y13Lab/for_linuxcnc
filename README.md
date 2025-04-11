### Для начинающих в LinuxCNC

Автоматический Вход <br />
sudo geany /etc/lightdm/lightdm.conf <br />
autologin-user=y13lab <br />

Изолирование Ядра <br />
sudo geany /etc/default/grub <br />
GRUB_CMDLINE_LINUX_DEFAULT="quiet isolcpus=3" <br />
обновить загрузчик <br />
sudo update-grub <br />
