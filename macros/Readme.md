### Macros

Макросы добавляются на вкладку MDI <br />

Создать папку macros в папке станка, <br />
в неё поместити ваши макросы. <br />

Добавить в Ваш станок.ini <br />

[MACROS] <br />
MACRO = go_to_home <br />
MACRO = go_to_zero <br />
MACRO = go_to_position <br />

[RS274NGC] <br />
SUBROUTINE_PATH = macros <br />
