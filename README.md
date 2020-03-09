# Google HTML/CSS Style Guide

Оглавление:

1.  [Описание](#1-описание "Описание")
1.  [Общее](#2-общее "Общее")
    * [Общие правила стиля](#21-общие-правила-стиля "Общие правила стиля")
      -  [Протокол](#211-протокол "Протокол")
    * [Общие правила форматирования](#22-общие-правила-форматирования "Общие правила форматирования")
      -  [Отступы](#221-отступы "Отступы")
      -  [Регистр](#222-регистр "Регистр")
      -  [Заканчивающий пробел](#223-заканчивающий-пробел "Заканчивающий пробел")
    * [Общие правила для метаданных](#23-общие-правила-для-метаданных "Общие правила для метаданных")
      - [Кодировка](#231-кодировка "Кодировка")
      - [Комментарии](#232-комментарии "Комментарии")
      - [Метки действий (Action Items)](#233-метки-действий-action-items "Метки действий (Action Items)")
1. [HTML](#3-html "HTML")
    * [Правила стиля HTML документов](#31-правила-стиля-html-документов "Правила стиля HTML документов")
      - [Тип документа](#311-тип-документа "Тип документа")
      - [Валидация HTML документа](#312-валидация-html-документа "Валидация HTML документа")
      - [Семантика](#313-семантика "Семантика")
      - [Резерв для элементов мультимедиа](#314-резерв-для-элементов-мультимедиа "Резерв для элементов мультимедиа")
      - [Разделение задач](#315-разделение-задач "Разделение задач")

# 1 Описание

Этот документ определяет правила форматирования и стиля для документов HTML и CSS. Он нацелен на содействие, качество кода и создании вспомогательной инфраструктуры. Это относится к любому типу файла, где используется HTML и CSS, включая и GSS файлы. С последним предложением я просто затупил.

# 2 Общее

## 2.1 Общие правила стиля

### 2.1.1 Протокол

Используйте протокол HTTPS для встраеваемых ресурсов где это возможно.

Всегда используйте HTTPS (https:) протокол для изображений и других медиа файлов, таблиц стилей и скриптов, кроме тех случаев, когда эти файлы недоступны через HTTPS.

*HTML:*

```html
<!-- Не рекомендуется: опущен протокол -->
<script src="//ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
<!-- Не рекомендуется: используется HTTP -->
<script src="http://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
```

```html
<!-- Рекомендуется -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js"></script>
```
  
*CSS:*

```css
/* Не рекомендуется: опущен протокол */
@import '//fonts.googleapis.com/css?family=Open+Sans';
/* Не рекомендуется: используется HTTP */
@import 'http://fonts.googleapis.com/css?family=Open+Sans';
```

```css
/* Рекомендуется */
@import 'https://fonts.googleapis.com/css?family=Open+Sans';
```

## 2.2 Общие правила форматирования

### 2.2.1 Отступы

Используйте 2 пробела в отступе.

Не используйте табуляцию или табуляцию с пробелами для отступов.

*HTML:*

```html
<ul>
  <li>Фантастически
  <li>Великолепно
</ul>
```

*CSS:*

```css
.example {
  color: blue;
}
```

### 2.2.2 Регистр

Используйте только нижний регистр.

Весь код должен быть в нижнем регистре. Это применяется к тегам HTML-элементов, аттрибутам, значениям аттрибутов (кроме `text/CDATA`), CSS селекторов, свойств и значений свойств (за исключением строк).

*HTML:*

```html
<!-- Не рекомендуется -->
<A HREF="/">Дом</A>
```

```html
<!-- Рекомендуется -->
<img src="google.png" alt="Google">
```

*CSS:*

```css
/* Не рекомендуется */
color: #E5E5E5;
```

```css
/* Рекомендуется */
color: #e5e5e5;
```

### 2.2.3 Заканчивающий пробел

Удалите заканчивающие строку пробелы.

Заканчивающие пробелы необязательны и могут усложнять сравнение файлов.

```html
<!-- Не рекомендуется -->
<p>Что?_
```

```html
<!-- Рекомендуется -->
<p>Да, пожалуйста.
```

## 2.3 Общие правила для метаданных

### 2.3.1 Кодировка

Используйте кодировку UTF-8 (не BOM).

Убедитесь, что ваш редактор использует символьную кодировку UTF-8 без метки порядка байтов.

Уточняйте кодировку HTML шаблонов и документов с помощью `<meta charset="utf-8">`. Не уточняйте кодировку каскадных таблиц стилей, так как она по умолчанию подразумевает UTF-8.

(Подробнее о кодировках, а также о том, когда и как их указывать, можно найти в разделе [Обработка кодировок символов в HTML и CSS (Eng)](https://www.w3.org/International/tutorials/tutorial-char-enc/ "Handling character encodings in HTML and CSS").)

### 2.3.2 Комментарии

Объясняйте код по возможности и где это возможно.

Используйте комментарии, чтобы объяснить код: что он охватывает, зачем он нужен, почему используется или применяется соответствующее решение?

(Этот элемент не является обязательным, поскольку не всегда возможно полностью задокументировать код. Его польза может сильно различаться для HTML и CSS-кода и зависит от сложности проекта.)

### 2.3.3 Метки действий (Action Items)

Помечайте задачи и метки для действий с помощью `TODO`.

Выделяйте задачи только меткой `TODO` и не используйте другие распространённые форматы по типу `@@`.

Добавьте контакт (имя пользователя или его почту) в скобках в формате `TODO(контакт)`.

Добавьте действие после двоеточия: `TODO: действие`.

```html
{# TODO(john.doe): Пересмотреть центрирование #}
<center>Тест</center>
```

```html
<!-- TODO: удалить необязательные теги -->
<ul>
  <li>Яблоки</li>
  <li>Апельсины</li>
</ul>
```

# 3 HTML

## 3.1 Правила стиля HTML документов

### 3.1.1 Тип документа

Используйте HTML5. 

HTML5 (HTML синтаксис) предпочтителен для всех документов HTML: `<!DOCTYPE html>`.

(Рекомендуется использовать HTML как `text / html`. Не используйте XHTML. У XHTML, как `application / xhtml + xml`, недостаточно хорошая браузерная и инфраструктурная поддержка и меньше возможностей для оптимизации, чем у HTML.)

Хотя это и не ошибка для HTML, не закрывайте пустые элементы, т.е. пишите `<br>`, а не `<br />`.

### 3.1.2 Валидация HTML документа

По возможности используйте валидный HTML документ.

Использование валидного HTML документа - это измеримый базовый атрибут качества, который помогает узнать технические требования и ограничения и обеспечивает правильное использование документа HTML.

Для тестирования используйте такие инструменты, как [W3C HTML validator](https://validator.w3.org/nu/ "W3C HTML validator").

```html
<!-- Не рекомендуется -->
<title>Тест</title>
<article>Это всео лишь тест.
```

```html
<!-- Рекомендуется -->
<!DOCTYPE html>
<meta charset="utf-8">
<title>Тест</title>
<article>Это всего лишь тест.</article>
```

### 3.1.3 Семантика
 
 Используйте HTML в соответствии с его назначением.

 Используйте элементы (иногда неверно называют "теги") для того, для чего они были созданы. Например, используйте элементы заголовка для заголовков, `p` элементы для параграфов, `a` элементы для ссылок и т.д.

 Использование HTML по назначению важно тем, что благодаря этому код более эффективен, доступен и пригоден для повторного использования.

 ```html
<!-- Не рекомендуется -->
<div onclick="goToRecommendations();">Все рекомендации</div>
 ```

 ```html
<!-- Рекомендуется -->
<a href="recommendations/">Все рекомендации</a>
 ```

 ### 3.1.4 Резерв для элементов мультимедиа

 Предоставляйте альтернативный контент для мультимедиа.

 Для мультимедиа, таких как изображения, видео, анимированные объекты, представленные с помощью элемента `canvas`, не забудьте предоставить альтернативный доступ к этим элементам. Для изображений используйте альтернативный текст ( `alt` ), а для видео и аудио транскрипты и подписи, если есть возможность.

 Предоставление алтернативного контента важно для доступности: у слепого пользователя не будет возможности узнать, что на изображении без `@alt`, а у других же пользователей не будет возможности понять о чём видео или аудио.

 (Для изображений, чей атрибут `alt` привносит избыточность в код и для тех изображений, которые служат исключительно для декоративных целей и для которых вы ещё не задали оформление, используйте пустой атрибут `alt=""`. )

 ```html
<!-- Не рекомендуется -->
<img src="spreadsheet.png">
 ```

```html
 <!-- Рекомендуется -->
<img src="spreadsheet.png" alt="Скриншот таблицы.">
```

### 3.1.5 Разделение задач

Отделяйте структуру документа от её представления и поведения.

Строго разделяйте структуру документа (разметку), представление (стилизации) и поведение (сценарии) и старайтесь свести взаимодействие между ними к абсолютному минимуму.

То есть убедитесь, что документы и шаблоны содержат только HTML, который служит исключительно структурным целям. Переместите всю стилизацию в таблицы стилей, а всё поведение - в сценарии.

Кроме того, не добавляйте в область контактов много разных ссылок, связывайте как можно меньше таблиц стилей и сценариев из документов и шаблонов.

Отделение структуры от представления и поведения необходимо для удобства обслуживания. Менять документы и шаблоны HTML всегда сложнее и дороже, чем обновлять таблицы стилей и скрипты.

```html
<!-- Не рекомендуется -->
<!DOCTYPE html>
<title>HTML отстой</title>
<link rel="stylesheet" href="base.css" media="screen">
<link rel="stylesheet" href="grid.css" media="screen">
<link rel="stylesheet" href="print.css" media="print">
<h1 style="font-size: 1em;">HTML отстой</h1>
<p>Я прочитал об этом на нескольких сайтах и с уверенностью заявляю:
  <u>HTML это тупость!!1</u>
<center>Не могу поверить, что стилизация моего сайта невозможна без переделывание всего заного.</center>
```

```html
<!-- Рекомендуется -->
<!DOCTYPE html>
<title>Мой первый редизайн только с помощью CSS</title>
<link rel="stylesheet" href="default.css">
<h1>Мой первый редизайн только с помощью CSS</h1>
<p>Я прочитал об этом на нескольких сайтах и сегодня я наконец сделаю это: я разделяю задачи и избегаю всего, что не относится к HTML на моём презентационном сайте.
<p>Это великолепно!
```

### 3.1.6 Ссылочные сущности

Не используйте ссылочные сущности.

Нет нужды использовать ссылочные сущности, такие как `&mdash;`, `&rdquo;` или `&#x263a;`, при условии, что ваши файлы и редакторы (включая всю команду разработчиков) используют одну и ту же кодировку (UTF-8).

Единственное исключение - символы с особым значением в HTML (такие как `<` и `&`), а также управляющие или "невидимые" символы (например, неразрывный пробел).

```html
<!-- Не рекомендуется -->
Символ валюты для евро &ldquo;&eur;&rdquo;.
```

```html
<!-- Рекомендуется -->
Сивол валюты для евро “€”.
```

### 3.1.7 Необязательные теги

Не пишите необязательные теги (опционально).

В целях оптимизации размера и возможности сканирования файла рекомендуется исключить необязательные теги. [Спецификация HTML5](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission "HTML5 Specification") определяет, какие теги можно не писать.

(Для этого подхода может потребоваться установка льготного периода и в качестве дальнего ориентира, поскольку он значительно отличается от того, что обычно учат веб-разработчики. Из соображений последовательности и простоты лучше всего пропустить все необязательные теги, а не просто их выборку.)

```html
<!-- Не рекомендуется -->
<!DOCTYPE html>
<html>
  <head>
    <title>Тратим деньги, тратим байты</title>
  </head>
  <body>
    <p>Именно так.</p>
  </body>
</html>
```

```html
<!-- Рекомендуется -->
<!DOCTYPE html>
<title>Экономим деньги, экономим байты</title>
<p>Что и требовалось доказать.
```

### 3.1.8 `type` атрибуты

Не пишите атрибут `type`  для таблиц стилей и скриптов.

Не используйте атрибут `type` для таблиц стилей (кроме тех случаев, если используете не CSS), и для скриптов (кроме тех случаев, если используете не JavaScript).

Определение атрибута `type` в этом контексте необязательно, так как HTML5 подразумевает `text/css` и `text/javascript` по умолчанию. Поэтому это безопасно и для старых браузеров.

```html
<!-- Не рекомендуется -->
<link rel="stylesheet" href="https://www.google.com/css/maia.css"
    type="text/css">
<!-- Не рекомендуется -->
<script src="https://www.google.com/js/gweb/analytics/autotrack.js"
    type="text/javascript"></script>
```

```html
<!-- Рекомендуется -->
<link rel="stylesheet" href="https://www.google.com/css/maia.css">
<!-- Рекомендуется -->
<script src="https://www.google.com/js/gweb/analytics/autotrack.js"></script>
```

## 3.2 Правила форматирования HTML

### 3.2.1 Общее форматирование

Используйте новую строку для каждого блока, листа или табличный элемент. Также не забывайте про отступы дочерних элементов.

Независимо от стилизации элемента (CSS позволяет элементам принимать различные позиции с помощью свойства `display`), пишите каждый блок, лист или табличный элемент с новой строки.

Кроме того, делайте правильный отступ, если они являются дочерними элементами блока, списка или табличного элемента.

(Если у вас возникают проблемы с пробелами между элементами списка, допустимо поместить все элементы `li` в одну строку. Линтер будет выдавать предупреждение, а не ошибку.)

```html
<blockquote>
  <p><em>Space</em>, the final frontier.</p>
</blockquote>
```

```html
<ul>
  <li>Мо
  <li>Ларри
  <li>Кёли
</ul>
```

```html
<table>
  <thead>
    <tr>
      <th scope="col">Доход
      <th scope="col">Налоги
  <tbody>
    <tr>
      <td>$ 5.00
      <td>$ 4.50
</table>
```

### 3.2.2 Перенос строки в HTML

Разделяйте длинные строки на более маленькие (опционально).

Хотя в HTML и нет рекомендации на лимит строк и столбцов, вы можете резделять длинные строки если это существенно улучшит читаемость.

При разделении строки, каждая последующая строка должна иметь отступ минимум 4 пробела от первоначальной строки.

```html
<md-progress-circular md-mode="indeterminate" class="md-accent"
    ng-show="ctrl.loading" md-diameter="35">
</md-progress-circular>
```

```html
<md-progress-circular
    md-mode="indeterminate"
    class="md-accent"
    ng-show="ctrl.loading"
    md-diameter="35">
</md-progress-circular>
```

```html
<md-progress-circular md-mode="indeterminate"
                      class="md-accent"
                      ng-show="ctrl.loading"
                      md-diameter="35">
</md-progress-circular>
```

### 3.2.3 Кавычки в HTML

Когда вы выделяете кавычками значения аттрибутов, используйте двойные кавычки.

Предпочитайте использовать двойные ( `""` ) кавычки вместо одинарных ( `''` ), когда выделяете значения атрибутов.

```html
<!-- Не рекомендуется -->
<a class='maia-button maia-button-secondary'>Войти</a>
```

```html
<!-- Рекомендуется -->
<a class="maia-button maia-button-secondary">Войти</a>
```

# 4 CSS

## 4.1 Правила стиля CSS

### 4.1.1 Валидация CSS

Используйте валидный CSS файл, когда это возможно.

Используйте валидный CSS файл, кроме тех случаев, когда вы встречаетесь с ошибками валидатора CSS или испольхуете собственный синтаксис.

Используйте инструменты, такие как [сервис проверки CSS от W3](https://jigsaw.w3.org/css-validator/ "W3C CSS validator"), для тестирования вашего кода.

Использование валидного кода CSS является базовым атрибутом качества. Он позволяет обнаружить CSS код, который не используется и может быть удалён, что обеспечивает правильное применение CSS.

### 4.1.2 Именование уникальных идентификаторов (ID) и классов

Используйте значимые и общие имена для уникальных идентификаторов и классов.

Вместо непонятных и загадочных имён, всегда используйте такие ID и классы, которые полностью отражают то, для чего необходим элемент. 

Имена, которые являются конкретными и отражают назначение элемента, должны быть предпочтительными, поскольку они наиболее понятны и которые, вероятно, не изменятся.

Общие имена просто запасные элементы, которые не имеют никакого особого отличия от похожих элементов. Они обычно нужны как «помощники» (хэлперы).

Использование функциональных (полностью отражающих назначение) или общих имен снижает вероятность ненужных изменений документа или шаблона.

```css
/* Не рекомендуется: бесспысленный ID */
#yee-1901 {}

/* Не рекомендуется: презентационное */
.button-green {}
.clear {}
```

```css
/* Рекомендуется: конкретное */
#gallery {}
#login {}
.video {}

/* Рекомендуется: общее */
.aux {}
.alt {}
```

