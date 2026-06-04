### NGCGUI Gmoccapy

Скопировать pyngcgui.ui в папку станка. <br />

В ваш станок.ini добавить: <br />

[DISPLAY] <br />
EMBED_TAB_NAME = NGCGUI <br />
EMBED_TAB_LOCATION = ntb_user_tabs <br />
EMBED_TAB_COMMAND = gladevcp -x {XID} pyngcgui.ui <br />
NGCGUI_SUBFILE = проточка.ngc <br />
NGCGUI_SUBFILE = расточка.ngc <br />
NGCGUI_SUBFILE = сверление.ngc <br />

[RS274NGC] <br />
SUBROUTINE_PATH = ngcgui <br />
если уже есть папка, например macros <br />
то папки пишем через : без пробелов. <br />
SUBROUTINE_PATH = macros:ngcgui <br />
