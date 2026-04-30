### Макросы для встройки в Gmoccapy

Макросы добавляются во вкладку MDI <br />

Создать папку macros в папке стака, <br />
в неё поместити ваши макросы. <br />

Добавить в Ваш станок.ini <br />

[RS274NGC] <br />
SUBROUTINE_PATH = macros <br />

[MACROS] <br />
MACRO = go_to_home <br />
MACRO = go_to_zero <br />
MACRO = go_to_position <br />
