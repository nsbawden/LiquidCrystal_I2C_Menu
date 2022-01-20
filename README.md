## LiquidCrystal_I2C_Menu
**LiquidCrystal_I2C_Menu** - это библиотека для создания пользовательского интерфейса на Ардуино и текстовом ЖК дисплее с I2C интерфейсом. Библиотека предоставляет функционал для форматированного вывода, ввода и выбора значений, организации меню. Управление осуществляется с помощью энкодера вращения с кнопкой.

## Подключение
[![LiquidCrystal_I2C_Menu Подключение](https://github.com/VladimirTsibrov/LiquidCrystal_I2C_Menu/raw/master/wiring/LiquidCrystal_I2C_Menu%20wiring.png "LiquidCrystal_I2C_Menu Подключение")](https://github.com/VladimirTsibrov/LiquidCrystal_I2C_Menu/raw/master/wiring/LiquidCrystal_I2C_Menu%20wiring.png "LiquidCrystal_I2C_Menu Подключение")

## Управление кнопками
Вместо энкодера вращения могут быть использованы кнопки. Для этого существует другая версия данной библиотеки - [LiquidCrystal_I2C_Menu_Btns](https://github.com/VladimirTsibrov/LiquidCrystal_I2C_Menu_Btns "LiquidCrystal_I2C_Menu_Btns")

## Функции

Below are library functions:

- **printAt(x, y, data)** – prints data from the specified position.
- **printf(format, …)** – prints formatted data. Works like sprintf, but unlike it prints data to the display, not to the buffer.
- **printfAt(x, y, format, …)** – prints formatted data from the specified position.
- **attachEncoder(pinA, pinB, pinBtn)** – tells the library which pins of the Arduino the encoder is connected to.
- **getEncoderState()** – polling the encoder status. Returns a value of type eEncoderState (an enumerated type, described in the library as {eNone, eLeft, eRight, eButton}).
- **printMultiline(text)** – prints text with vertical scrolling.
- **inputVal(title, min, max, default, [step], [onChangeFunc])** – entering a numeric value. The min and max parameters specify the range in which the value can change; default - initial value; step - the value of the increment, by the default is 1; optional parameter onChangeFunc - a pointer to a function that should be called when the value changes.
- **inputValAt(x, y, min, max, default, [step], [onChangeFunc])** – is similar to the inputVal function, but unlike it, it does not clear the display when called and the value is entered from the specified position.
- **inputValBitwise(title, value, precision, [scale], [signed])** – allows you to enter values by editing individual digits of a number. The value parameter is a reference to the variable into which the result will be placed; precision - total number of digits in a number; scale - the number of digits to the right of the decimal point, the default value is 0; signed - allows (if true) or disallows (if false - by default) entering negative numbers. The function returns true if the user confirmed the input, false if he refused.
- **inputStrVal(title, buffer, length, available_symbols)** – unlike inputValBitwise allows you to enter not only numeric values. buffer - a reference to a character buffer, into which the result of the input will be placed; length - the number of characters to enter; the available_symbols parameter is the string of characters available for input.
- **selectVal(title, list_of_values, count, [show_selected], [selected_index])** – lets you select a value from the list and returns the index of the selected item. list - a list of values to select, is an array of char*, String or int values; count - the number of elements in the array; show_selected - flag for displaying the label on the selected element; selected_index - the index of the default selected item.
- **showMenu(menu, menu_length, show_title)** – displays the menu and returns the key of the selected item. menu is an array of items of sMenuItem type; menu_length - length of the menu; show_title - flag to display the title.
- **getSelectedMenuItem()** – returns the key of the selected menu item for use inside menu-handlers.
- **attachIdleFunc(IdleFunc)** – allows you to bind a function that will be called by the library when idle.


## Поддержка дисплеев с кириллицей
Для включения поддержки дисплеев с кириллицей необходимо в файле LiquidCrystal_I2C_Menu.h раскомментировать строку #define CYRILLIC_DISPLAY. После этого станет возможным использование русского текста в меню и других функциях библиотеки.


## Более подробно
Более подробную информацию о библиотеке и её функциях вы найдете здесь: [https://tsibrov.blogspot.com/2020/09/LiquidCrystal-I2C-Menu.html](https://tsibrov.blogspot.com/2020/09/LiquidCrystal-I2C-Menu.html "https://tsibrov.blogspot.com/2020/09/LiquidCrystal-I2C-Menu.html")
