# Лабораторная работа №9. Адаптивная верстка: Медиа-запросы

## Цель работы
Изучить принципы адаптивной верстки с помощью Flexbox и Grid. В ходе работы создается адаптивная страница портфолио, которая корректно отображается на всех устройствах.

## Задачи
- Реализовать адаптивное меню с помощью Flexbox.
- Создать страницу с секциями, которые адаптируются под различные размеры экранов.
- Использовать медиа-запросы для изменения стилей при изменении ширины окна браузера.
- Обеспечить корректное отображение элементов на мобильных, планшетных и десктопных устройствах.

## Структура проекта
- `responsive.html` — HTML-страница с разметкой.
- `responsive.css` — стили для `responsive.html`.
- `nav-practice.html` —  страница для практики.
- `nav.css` — Стили для `nav-practice.html`.
- `flexbox-practice.html` — страница для flexbox макета
- `flexbox.css` — стили для `flexbox-practice.html`
- Есть комментарии и примеры кода для пояснения.

## Основные моменты реализации
- Использование Flexbox для оформления навигационного меню и шапки сайта.
- Использование Grid для расположения секций с карточками
- Медиа-запросы для изменения компоновки с колонок на мобильных и планшетных устройствах.
- Адаптация элементов, таких как меню, карточки и секции, под разные разрешения экранов.

## Структура файла `responsive.html`

В файле `responsive.html` реализована структура сайта с использованием современных стандартов и подходов:

- В `<header class="header">` — навигационное меню с логотипом.
- В основном блоке `<main class="main">` — секции с контентом:
  - `hero` — приветственное сообщение с градиентным фоном.
  - `features` — три блока с описанием основных технологий
  - `cards` — сетка карточек с изображениями и описаниями.
- В конце — `<footer class="footer">` — подвал сайта с информацией о копирайте.

---
### HTML структура

```html
<!DOCTYPE html>
<html lang="ru-RU">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Адаптивный макет</title>
    <link rel="stylesheet" href="responsive.css" />
</head>
<body>
    <header class="header">
        <div class="logo">Логотип</div>
        <nav class="nav">
            <a href="#">Главная</a>
            <a href="#">Услуги</a>
            <a href="#">Портфолио</a>
            <a href="#">Контакты</a>
        </nav>
    </header>
    <main class="main">
        <section class="hero">
            <h1>Добро пожаловать!</h1>
            <p>Адаптивная верстка на Flexbox и Grid</p>
        </section>
        <section class="features">
            <div class="feature">
                <h3>Flexbox</h3>
                <p>Одномерная раскладка для меню, карточек</p>
            </div>
            <div class="feature">
                <h3>Grid</h3>
                <p>Двумерная сетка для сложных макетов</p>
            </div>
            <div class="feature">
                <h3>Media Queries</h3>
                <p>Адаптация под любые устройства</p>
            </div>
        </section>
        <section class="cards">
            <article class="card">
                <img src="https://via.placeholder.com/300x200" alt="Изображение 1" />
                <h3>Карточка 1</h3>
                <p>Описание первой карточки</p>
            </article>
            <article class="card">
                <img src="https://via.placeholder.com/300x200" alt="Изображение 2" />
                <h3>Карточка</h3>
                <p>Описание второй карточки</p>
            </article>
            <article class="card">
                <img src="https://via.placeholder.com/300x200" alt="Изображение 3" />
                <h3>Карточка 3</h3>
                <p>Описание третьей карточки</p>
            </article>
        </section>
    </main>
    <footer class="footer">
        <p>&copy; 2026 Адаптивная верстка. Все права защищены.</p>
    </footer>
</body>
</html>
```

## Структура файла `nav-practice.html`
В файле `nav-practice.html` реализована структура сайта с использованием современных стандартов:
- В шапке (`<nav class="menu">`) — навигационное меню с ссылками.
- В основном блоке — секции с контентом.
- В конце страницы — подвал сайта (`<footer class="footer">`) с информацией о копирайте:
- Подвал сайта - то место где расположена доп. информация, копирайты, ап и т.д

```html
    <footer class="footer">
        <p>&copy; 2026 Адаптивная верстка. Все права защищены.</p>
    </footer>
```

## Структура файла `flexbox-practice.html`

В файле `flexbox.html` реализована структура сайта с использованием Flexbox для построения адаптивной и гибкой верстки:

- В `<header class="header">` — логотип и навигационное меню.
- В основном разделе `<section class="about-section">` — секция "О нас" с тремя карточками, каждая из которых содержит иконку, заголовок и описание.
- В конце — `<footer class="footer">` — подвал сайта с копирайтом.

---

## Описание основных частей кода

### HTML структура

```html
<!DOCTYPE html>
<html lang="ru-RU">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Практика Flexbox</title>
    <link rel="stylesheet" href="flexbox.css" />
    <!-- подключил иконки, чтобы было по прикольней-->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" />
</head>
<body>
    <header class="header">
        <div class="logo">Лого</div>
        <nav class="navigation">
            <a href="#">Главная</a>
            <a href="#">Услуги</a>
            <a href="#">Портфолио</a>
            <a href="#">Контакты</a>
        </nav>
    </header>
    
    <section class="about-section">
        <h2 class="about-title">О нас</h2>
        <div class="about-cards">
            <!-- первая -->
            <div class="about-card">
                <i class="icon fa fa-briefcase"></i>
                <h3 class="card-title">Наша деятельность</h3>
                <p class="card-text">text and text, more text</p>
            </div>
            <!-- вторая -->
            <div class="about-card">
                <i class="icon fa fa-users"></i>
                <h3 class="card-title">Наша команда</h3>
                <p class="card-text">text and text, more text</p>
            </div>
            <!-- третья -->
            <div class="about-card">
                <i class="icon fa fa-cubes"></i>
                <h3 class="card-title">Наша продукция</h3>
                <p class="card-text">text and text, more text</p>
            </div>
        </div>
    </section>
    <footer class="footer">
        <p>&copy; 2026</p>
    </footer>
</body>
</html>
```
## Итоги
В результате выполненной работы создана адаптивная страница, которая отображается как на мобильных устройствах, так и на больших экранах


## Используемые технологии
- HTML
- CSS
- Flexbox
- Grid
- Медиа-запросы