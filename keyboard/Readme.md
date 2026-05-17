### Keyboard

Установить matchbox-keyboard с помощью менеджера пакетов Synaptic

Создать папку для своей темы matchbox-keyboard, <br />
в терминале ввести mkdir ~/.matchbox <br />
Скопировать туда свою тему keyboard.xml <br />

Если уже установлена виртуальная клавиатура Onboard <br />
но хочется чтобы в LinuxCNC была matchbox-keyboard, <br />
надо сделать её приорететной в gmoccapy. <br />
в терминале ввести sudo geany /usr/bin/gmoccapy <br />
Примерно с 1946 по 1971 строку заменить на <br />

    # shows "Onboard" virtual keyboard if available
    # else error message
    def _init_keyboard(self, args="", x="", y=""):
        self.onboard = False

        # now we check if onboard or matchbox-keyboard is installed
        try:
            if os.path.isfile("/usr/bin/matchbox-keyboard"):
                self.onboard_kb = subprocess.Popen(["matchbox-keyboard", "--xid"],
                                                   stdin=subprocess.PIPE,
                                                   stdout=subprocess.PIPE,
                                                   close_fds=True)
                print (_("**** GMOCCAPY INFO ****"))
                print (_("**** virtual keyboard program found : <matchbox-keyboard>"))
            elif os.path.isfile("/usr/bin/onboard"):
                self.onboard_kb = subprocess.Popen(["onboard", "--xid", args, x, y],
                                                   stdin=subprocess.PIPE,
                                                   stdout=subprocess.PIPE,
                                                   close_fds=True)
                print (_("**** GMOCCAPY INFO ****"))
                print (_("**** virtual keyboard program found : <onboard>"))
            else:
                print (_("**** GMOCCAPY INFO ****"))
                print (_("**** No virtual keyboard installed, we checked for <onboard> and <matchbox-keyboard>."))
                self._no_virt_keyboard()
                return
