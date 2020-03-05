# 1. Описание
# 2. Общее
## 2.1 Общие правила стиля
### 2.1.1 Протокол
Используйте протокол HTTPS для встраеваемых ресурсов где это возможно.
Всегда используйте HTTPS (https:) протокол для изображений и других медиа файлов, таблиц стилей и скриптов, кроме тех случаев, когда эти файлы недоступны через HTTPS.

    *<!-- Не рекомендуется: опущен протокол -->*
    <script src="//ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    *<!-- Не рекомендуется: используется HTTP -->*
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
  
    */* Не рекомендуется: опущен протокол */*
    @import '//fonts.googleapis.com/css?family=Open+Sans';
    /* Не рекомендуется: используется HTTP */
    @import 'http://fonts.googleapis.com/css?family=Open+Sans';
  
    *<!-- Рекомендуется -->*
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
    */* Рекомендуется */*
    @import 'https://fonts.googleapis.com/css?family=Open+Sans';
