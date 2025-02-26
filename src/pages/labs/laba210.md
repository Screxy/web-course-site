---
layout: "../../layouts/BaseLayout.astro"
title: "Лабораторная работа №10"
tag: "2 семестр"
---

## Fetch API

**Цель:** изучение формата обмена данными JSON, возможностей Fetch API.

## Содержание и порядок выполнения лабораторной работы:

1. Изучить работу с форматом данных JSON и глобальным объектом, изучить возможности Fetch API (`fetch()`, `Response`).
1. Создать новую страницу fetch.html в проекте из предыдущих лабораторных работ. Добавить ссылку на эту страницу в меню макета.
1. К fetch.html подключить вашу "нанобиблиотеку" из 4-й работы и добавить две секции: для галереи и отправки температуры.
1. Модифицируйте компонент сообщений (toasts) из 7-й работы, чтобы для ошибок фон был красный, для сообщений - зеленый.
1. [Сервер с документацией](http://slavaver.space/api/).

### Галерея

1. В галерее, используя AJAX, после загрузки страницы отправить запрос на получение изображений и отобразить их на странице. Если возникают какие-либо ошибки оповестить об этом пользователя с помощью компонента toast. На время пока ожидается ответ от сервера, показать загрузчик, после получения ответа загрузчик должен замениться на контент или должно появится сообщение об ошибке. Если пришел пустой массив, то на месте галереи должен отображаться текст "Изображения не найдены".
1. В начало этой же секции, добавить кнопку обновления, при нажатии на которую отправляет запрос на получение изображений, а работа с ошибками сохраняется как в предыдущем пункте.
1. Все блоки изображений с подписями должны выглядеть одинаково, не смотря на размер изображения или длину текста. В один ряд помещается 4-изображения для этого используйте гриды из "нанобиблиотеки".

### Температура

1. В этой секции добавить форму для ввода номера аудитории и температуры. Не забудьте про доступность.
1. Для отправки данных из формы предотвратите стандартное поведение формы, сформируйте собственный post-запрос с помощью fetch. Не забудьте в заголовках указать тип передаваемого контента (Content-Type) и отправить данные с правильными типами (строка и число).
1. На время ожидания ответа от сервера заблокируйте возможность отправлять новые запросы из формы.
1. При успешной обработке данных на сервере с помощью toast выведите сообщение из ответа и очистите форму. При ошибке, выведите сообщение ошибки в toast, но форму не очищайте.

### Результаты выполнения лабораторной работы:

Результаты работы _проверены наставником_.

Статическая веб-страница на хостинге проверенная, со структурой и оформлением, которая соответствует требованиям и сохранена в системе контроля версий.

## Источники

- [Fetch API](https://developer.mozilla.org/ru/docs/Web/API/Fetch_API)
- [RFC8259: The JavaScript Object Notation (JSON) Data Interchange Format](https://datatracker.ietf.org/doc/html/rfc8259)
- [ECMA-404: The JSON data interchange syntax](https://www.ecma-international.org/publications-and-standards/standards/ecma-404/)
- [ECMA-262: JSON5](https://262.ecma-international.org/11.0/#sec-json-object)
- [Библиотека Axios](https://github.com/axios/axios)

## Вопросы для защиты

1. Суть AJAX
1. Что такое и как работает Fetch API
1. На базе чего построен Fetch API
1. Какие есть свойства и методы у объекта Response
1. Какие методы из DOM позволяют создавать и добавлять элементы
