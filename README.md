# Тестовое задание

В рамках тестового задания необходимо сделать небольшое SPA на Vue3(options API). Приложение включает в себя: форму создания запроса на парсинг фриланс бирж и страницу вывода спаршенных данных на которой нужно выполнять crud-операции с ними.

## Демонстрация выполненного задания

[compas.oreshkin.dev](https://compas.oreshkin.dev/)

### Задание

Форма включает в себя:

-   Выбор биржи (freelance, kwork, выбрать все)
-   Ввод ключевых слов по которым происходит парсинг, например, spring boot, hibernate и т.п.

Страница состоит из списка карточек спаршенных объявлений и данных о конкретном парсере. В карточке необходимо реализовать функционал редактирования данных (заголовок и тело объявления), удаления карточки.
Валидация форм необязательна для этого тестового, но если будет реализовано - отлично, использование сторонних библиотек - хорошо.
Дизайн не принципиален, но нужно показать свои навыки работы с версткой и работу с api.

### Интеграция с API

Мы предоставляем частичное апи одного из наших сервисов. [Получить документацию по этому апи:](https://parser.api-compas-goo.ru/swagger/)

### Для доступа используй ключ-апи:

```
{"Authorization": "Api-Key VSfHLDHK.MM3MeLZNV9HMDEY5s1zz4Yl79lbRwoux"}
```

Т.к. сервис является частью системы, то в его использовании возникают следующие условности:
При создании запроса на парсинг можно указывать любые уникальные целочисленные неотрицательные значения в полях:

-   id_parsource, id_user и любую уникальную строку в поле hash_parsource.
-   Поле sources принимает массив целых чисел в диапазоне от 1 до 2, но по сути это enum, где 1 представляет значение freelance, 2 - kwork.

### Группа ручек по работе с запросами на парсинг - /parser-config/

С данными, полученными от группы эндпоинтов /api/{наименование биржи}/ Можно выполять любые CRUD, в приципе, в Swagger всё описано, если будут вопросы - можно написать в ТГ.

### Стек

По технологиям - на выбор, неизменно лишь vue3 в options исполнении, vue-router и если понадобится стейт менеджер, то vuex. Т.к. это стек всех наших проектов. Препроцессор sass в синтаксисе scss. Создание и сборка у нас на vue-cli.

## Установка

```
npm i
/
yarn
```

### Compiles and hot-reloads for development

```
npm run serve
/
yarn serve
```

### Compiles and minifies for production

```
npm run build
/
yarn build
```
