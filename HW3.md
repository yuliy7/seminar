# Синтаксис языка MarkDown

## 1. Выделение заголовков

* Для того чтобы выделить заголовок нужно использовать символ "#"

* Колличество символов "#" задает уровень заголовка (поддерживается до 6 уровней)

* Также можно использовать символы "=" или "-" - подчеркиванием этими символами (не менее трех подряд) задает заголовки первого и второго порядка соответственно 

## 2. Редактирование текста

### 2.1. Курсивное начертание текста

Курсивом можно выделить текст с помощью обрамления текста символами "*" или "_"

Пример: *Курсив* и _Курсив_  

### 2.2. Полужирнре начертание текста

Обрамление текста двумя символами "*" или "_" делает его полужирным

Пример: **Полужирный текст** и __Полужирный текст__ 

### 2.3. Полужирное курсивное начертание текста

Обрамление текста тремя символами "*" или "_" делает его полужирным курсивом

Пример: ***Полужирный курсив*** и ___Полужирный курсив___ 

### 2.4. Зачеркнутый текст

Чтобы зачеркнуть текст нужно обрамить его двумя символами "~"

Пример: ~~Зачеркнутый текст~~

## 3. Создание списков

### 3.1 Нумерованные списки

Нумерованные списки создаются с помощию цифр 1, 2, 3 и т.д.

Пример: 

1. Первый элемент списка
2. Второй элемент списка
3. Третий элемент списка

### 3.2 Ненумерованные списки

Ненумерованный список создается при помощи установки символа "*" с пробелом в начале строки

Пример:

* Первый элемент списка
* Второй элемент списка
* Третий элемент списка

## Примечание.

Для того чтобы текст для пользователя перешел на новую строку необходимо пропустить одну строку в редакторе

Пример: 

Строка 

пропущена

Строка
не пропущена

Весь текст на обной строке

# Возможности изученные самостоятельно

## Создание цитат

Цитаты задаются угловой скобкой ">".

> Это строка является цитатой.

Здесь цитата прерывается.

> Можно писать много текста, и он автоматически преобразуется в одну цитату. Также можно использовать разилчные *начертания* в **цитате**. 

## Работа с изображениями

Чтобы вставить изображение в текст нужно написать следующее: 

![Это мой пес Принц](Prince.jpg)

# Домашнее задание №2

## Горизонтальные линии (разделители)

Для того чтобы создать горизонтальную линию с использованием синтаксиса языка Markdown, необходимо поместить три (или более) дефиса или звездочки на отдельной строке текста. 

Горизонтальные линии в Markdown выглядят следующим образом:

*Первая часть текста, который необходимо разделить*
***
*Вторая часть текста, который необходимо разделить*

Или

*__Первая часть текста, который необходимо разделить__*

---

*__Вторая часть текста, который необходимо разделить__*

При использовании символа дефис необходимо после первой части текста и перед второй оставлять пустую строку. Если этого не сделать, на экран будет выведен заголовок второго уровня и строка обычного текста. При использовании символа звездочки данным правилом можно пренебречь.

__Первая часть текста, который необходимо разделить__
---
__Вторая часть текста, который необходимо разделить__

## Ссылки

Markdown поддерживает два стиля оформления ссылок:

* Гиперссылка, с немедленным указанием адреса (внутритекстовая)
* Гиперссылка, подобная сноске

### __Гиперссылка, с немедленным указанием адреса (внутритекстовая)__

Подразумевается, что помимо URL-адреса существует еще текст ссылки. Он заключается в квадратные скобки. 
Для создания внутритекстовой гиперссылки необходимо использовать круглые скобки сразу после закрывающей квадратной. Внутри них необходимо поместить URL-адрес. В них же возможно расположить название, заключенное в кавычки, которое будет отображаться при наведении, но этот пункт не является обязательным.

[пример](http://example.com/ "Необязательная подсказка")

При ссылке на локальную директорию возможно использование относительного пути (от текущей страницы, сайта и т.п.)

### __Гиперссылка, подобная сноске__

При создании сносной гиперссылки вместо целевого адреса используется вторая пара квадратных скобок, внутри которых помещается метка, идентификатор ссылки (id).

[пример][id]:

Также, можно использовать пробел, чтобы отделять 2 пары квадратных скобок:

[пример] [id]:

В этом случае возможно определить идентификатор в любом месте документа:

[id]: http://example.com/ "Необязательная подсказка"

В результате на экран выводится следующее: 

[пример][id]: 

Иными словами, она состоит из следующих элементов:

* Идентификатор ссылки, окружённый квадратными скобками (которым может предшествовать необязательный отступ от одного до трёх пробелов);
* Двоеточие;
* Один или несколько пробелов (или символов табуляции);
* URL гиперссылки;
* Необязательный заголовок (подсказка к изображению, которая всплывает при наведении на него) гиперссылки, заключённый либо в двойные или одиночные кавычки, либо в скобки.

Идентификаторы ссылок могут состоять из букв, цифр, пробелов и знаков пунктуации, однако они не чувствительны к регистру. То есть эти два варианта эквивалентны:

[текст ссылки][a]

[текст ссылки][A]

Markdown позволяет также использовать неявно выраженный идентификатор (сокращенный). В этом случае метка не приводится, вместо неё текст гиперссылки используется и в качестве её имени, а вторая пара квадратных скобок остаётся пустою. Например, чтобы сделать слово «Example» гиперссылкой, ведущей на сайт http://example.com/, достаточно написать:

[Example][]

и затем определить гиперссылку: 

[Example]: http://example.com/ "Необязательная подсказка"

В результате на экран выводится следующее: 

[Example][] 

# Параграфы и разрывы строк

Для того, чтобы создать параграф с использованием синтаксиса языка Markdown, достаточно отделить строки текста одной (или более) пустой строкой (пустой считается всякая строка, которая не содержит в себе ничего, кроме пробелов и символов табуляции). 

Для того, чтобы вставить видимый перенос строки (элемент <br/>) необходимо окончить строку двумя пробелами и нажатием клавиши «Enter».  
Вот так
# Блоки кода и кодовые фрагменты строк

## блоки кода

Отформатированные блоки кода используются в случае необходимости процитировать исходный код программ или разметки. Для создания блока кода в языке Markdown необходимо каждую строку параграфа начинать с отступа, состоящего из четырех пробелов или одного символа табуляции. Блок кода продолжается до тех пор, пока не встретится строка без отступа (или конец текста). Внутри блока кода амперсанды («&») и угловые скобки («<» и «>») автоматически преобразуются в элементы HTML разметки. Кроме того, следует отметить, что внутри блоков кода обычный синтаксис Markdown не обрабатывается. Блок кода в Markdown выглядит следующим образом:

Это обычный параграф

    Это блок кода

## Кодовые фрагменты строк

Чтобы отметить фрагмент строки, содержащий код, необходимо окружить его обратными апострофами «`». При использовании кодовых фрагментов строк текст будет отображаться в виде моноширинного шрифта. В отличие от блоков кода, кодовый фрагмент позволяет поместить код внутрь обычного абзаца текста. Кодовый фрагмент строки в языке Markdown выглядит следующим образом:

Используйте оператор `if`

# Команды GIT

*git init* - **инициализировать локального репозитория**
*git status* – **получить информацию от git о его текущем состоянии**
*git add* – **добавить файл или файлы к следующему коммиту**
*git commit* – **m “massage” - создание коммита**
*git log* – **вывод на экран истории всех коммитов с их хеш-кодами**

# Команды для удаленного репозитория
*git clone* - **клонирование удаленного репо на локальный компьютер**
*git push* - **отправка изменений с локального на уленный компьютер**
*git pull* - ** стягивание изменений с удаленного репо на локальный компьютер**
