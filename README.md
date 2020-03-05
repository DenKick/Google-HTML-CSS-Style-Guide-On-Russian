# 1. Описание
This document defines formatting and style rules for HTML and CSS. It aims at improving collaboration, code quality, and enabling supporting infrastructure. It applies to raw, working files that use HTML and CSS, including GSS files. Tools are free to obfuscate, minify, and compile as long as the general code quality is maintained.
Этот документ определяет правила форматирования и стиля для документов HTML и CSS. Он нацелен на содействие, качество кода и создании вспомогательной инфраструктуры. Это относится к любому типу файла, где используется HTML и CSS, включая и GSS файлы. С последним предложением я просто затупил.
# 2. Общее
## 2.1 Общие правила стиля
### 2.1.1 Протокол
Используйте протокол HTTPS для встраеваемых ресурсов где это возможно.
Всегда используйте HTTPS (https:) протокол для изображений и других медиа файлов, таблиц стилей и скриптов, кроме тех случаев, когда эти файлы недоступны через HTTPS.

*HTML:*

    <!-- Не рекомендуется: опущен протокол -->
    <script src="//ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    *<!-- Не рекомендуется: используется HTTP -->*
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
  
*CSS:*
  
    /* Не рекомендуется: опущен протокол */
    @import '//fonts.googleapis.com/css?family=Open+Sans';
    /* Не рекомендуется: используется HTTP */
    @import 'http://fonts.googleapis.com/css?family=Open+Sans';
    
Рекомендации:
  
    <!-- Рекомендуется -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    /* Рекомендуется */
    @import 'https://fonts.googleapis.com/css?family=Open+Sans';

## 2.2 Общие правила форматирования
### 2.2.1 Отступы
Используйте 2 пробела в отступе.
Не используйте табы или табы и пробелы для отступов.

*HTML:*

    <ul>
      <li>Fantastic
      <li>Great
    </ul>
    
*CSS:*

    .example {
      color: blue;
    }
