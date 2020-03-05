# Google HTML/CSS Style Guide

# 1 Описание
Этот документ определяет правила форматирования и стиля для документов HTML и CSS. Он нацелен на содействие, качество кода и создании вспомогательной инфраструктуры. Это относится к любому типу файла, где используется HTML и CSS, включая и GSS файлы. С последним предложением я просто затупил.
# 2 Общее
## 2.1 Общие правила стиля
### 2.1.1 Протокол
Используйте протокол HTTPS для встраеваемых ресурсов где это возможно.
Всегда используйте HTTPS (https:) протокол для изображений и других медиа файлов, таблиц стилей и скриптов, кроме тех случаев, когда эти файлы недоступны через HTTPS.

*HTML:*

    <!-- Не рекомендуется: опущен протокол -->
    <script src="//ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    *<!-- Не рекомендуется: используется HTTP -->*
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>

    <!-- Рекомендуется -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
  
*CSS:*
  
    /* Не рекомендуется: опущен протокол */
    @import '//fonts.googleapis.com/css?family=Open+Sans';
    /* Не рекомендуется: используется HTTP */
    @import 'http://fonts.googleapis.com/css?family=Open+Sans';
  
    /* Рекомендуется */
    @import 'https://fonts.googleapis.com/css?family=Open+Sans';

## 2.2 Общие правила форматирования
### 2.2.1 Отступы
Используйте 2 пробела в отступе.
Не используйте табуляцию или табуляцию с пробелами для отступов.

*HTML:*

    <ul>
      <li>Fantastic
      <li>Great
    </ul>
    
*CSS:*

    .example {
      color: blue;
    }

### 2.2.2 Регистр
Используйте только нижний регистр.
Весь код должен быть в нижнем регистре. Это применяется к тегам HTML-элементов, аттрибутам, значениям аттрибутов (кроме `text/CDATA`), CSS селекторов, свойств и значений свойств (за исключением строк).

*HTML*

    <!-- Не рекомендуется -->
    <A HREF="/">Home</A>

    <!-- Рекомендуется -->
    <img src="google.png" alt="Google">

*CSS*

    /* Не рекомендуется */
    color: #E5E5E5;

    /* Рекомендуется */
    color: #e5e5e5;

### 2.2.3 Заканчивающий пробел
Удалите заканчивающие строку пробелы.
Заканчивающие пробелы необязательны и могут усложнять сравнение файлов.

    <!-- Не рекомендуется -->
    <p>What?_

    <!-- Рекомендуется -->
    <p>Yes please.

## 2.3 Общие правила для метаданных
### 2.3.1 Кодировка
Используйте кодировку UTF-8 (не BOM).
Убедитесь, что ваш редактор использует символьную кодировку UTF-8 без метки порядка байтов.
Уточняйте кодировку HTML шаблонов и документов с помощью `<meta charset="utf-8">`. Не уточняйте кодировку каскадных таблиц стилей, так как она по умолчанию подразумевает UTF-8.

//TODO: Прикрепить ссылку.

### 2.3.2 Комментарии
Объясняйте код по возможности и где это возможно.
Используйте комментарии чтобы объяснить код: что он охватывает, зачем он нужен, почему используется или применяется соответствующее решение?
(Этот элемент не является обязательным, поскольку не всегда возможно полностью задокументировать код. Его польза может сильно различаться для HTML и CSS-кода и зависит от сложности проекта.)

### 2.3.3 Метки действий (Action Items)
Помечайте задачи и метки для действий с помощью `TODO`.
Выделяйте задачи только меткой `TODO` без других распространённых форматов типа `@@`.
Добавьте контакт (имя пользователя или почтовый список) в скобках в формате `TODO (контакт)`.
Добавьте метки действий после двоеточия: `TODO: действие`.

    {# TODO(john.doe): revisit centering #}
    <center>Test</center>

    <!-- TODO: remove optional tags -->
    <ul>
      <li>Apples</li>
      <li>Oranges</li>
    </ul>
    
# 3 HTML
