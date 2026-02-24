# Лабораторная работа №9. Адаптивная верстка: Медиа-запросы

**Студент:** Катаржин Г.М.

**Группа:** ИСП-232

---
## Описание
Лабораторная работа посвящена изучению принципов адаптивной верстки и медиа-запросов (Media Queries). В ходе работы был создан адаптивный макет страницы портфолио, который корректно отображается на мобильных устройствах, планшетах и десктопах. Реализован подход "Mobile First", использованы технологии Flexbox для одномерной раскладки и CSS Grid для двумерных сеток.

---
## Технологии
- HTML5
- CSS3
- Flexbox
- CSS Grid
- Media Queries
---

## Структура проекта
* img - папка со скриншотами
* index.html 
* responsive.html - Страница с адаптивным макетом
* responsive.css - Стили для адаптивного макета
* nav-practice.html - Практическое задание №1 (Навигация)
*flexbox-practice.html - Практическое задание №2 (Flexbox макет)
* style.css - Примеры стилей
* README.md - Документация проекта

--- 
## Примеры кода (Media Queries)
Реализация адаптивности через контрольные точки (breakpoints):
```css
/* Базовые стили (Mobile First) */
.cards {
    display: grid;
    grid-template-columns: 1fr; /* 1 колонка на мобильных */
    gap: 20px;
}

/* Планшеты (от 768px) */
@media (min-width: 768px) {
    .header {
        flex-direction: row; /* Горизонтальный хедер */
        justify-content: space-between;
    }
    .cards {
        grid-template-columns: repeat(2, 1fr); /* 2 колонки */
    }
}

/* Десктопы (от 992px) */
@media (min-width: 992px) {
    .hero h1 {
        font-size: 48px;
    }
    .cards {
        grid-template-columns: repeat(3, 1fr); /* 3 колонки */
    }
    .main {
        max-width: 1200px;
        margin: 0 auto;
    }
}
```
---
## Лицензия 
Проект создан в  учебных целях.