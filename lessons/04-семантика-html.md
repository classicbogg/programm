# Урок 4. Семантическая разметка

**Часть:** HTML  
**Результат:** визитка с header, main, section, footer.
**Сколько примерно займёт:** 60–90 минут.

## Минимум урока

- Перестроить страницу в семантические блоки
- Использовать `nav` для навигации
- Оставить только один `main`

---

## Прочитать

| № | Статья на Доке |
|---|----------------|
| 1 | [Что такое семантика?](https://doka.guide/html/semantics/) |
| 2 | [`<header>`](https://doka.guide/html/header/) |
| 3 | [`<nav>`](https://doka.guide/html/nav/) |
| 4 | [`<main>`](https://doka.guide/html/main/) |
| 5 | [`<section>`](https://doka.guide/html/section/) |
| 6 | [`<article>`](https://doka.guide/html/article/) |
| 7 | [`<footer>`](https://doka.guide/html/footer/) |
| 8 | [`<div>`](https://doka.guide/html/div/) |
| 9 | [Атрибут `class`](https://doka.guide/html/class/) |
| 10 | [Глобальные атрибуты](https://doka.guide/html/global-attrs/) |

---

## Главное

- Семантика = тег описывает **роль** блока.
- `<main>` — один на страницу.
- `id` уникален; `class` — можно повторять.

**Emmet для шапки:**

```
header>h1+nav>ul>li*2>a
```

Разверни и подставь свои ссылки.

### Плохо / Хорошо

```html
<div class="header">
  <div class="nav">...</div>
</div>

<header>
  <nav>...</nav>
</header>
```

---

## Практика

Перестрой `index.html`: `header` → `main` с двумя `section` → `footer`.  
В `nav` — ссылки на `index.html` и `contact.html` (вторая страница — в уроке 5).

### Дополнительно

Одну карточку навыка оберни в `article` внутри `section`.

---

## Сдать после урока

- В `index.html` используются `header`, `main`, `section`, `footer`
- Навигация вынесена в `nav`
- В структуре страницы только один `main`

---

## Переход к следующему уроку

Переходи к уроку 5, только если:

1. Можешь объяснить, зачем семантика
2. Понимаешь разницу `div` и `section`
3. Страница читается как логичные блоки

---

## Проверь себя

1. Чем `section` отличается от `div`?
2. Сколько `main` на странице?
3. Когда использовать `article`?

---

## Самопроверка

- [ ] header, main, footer на месте
- [ ] main один
- [ ] nav внутри header

**Дальше:** [Урок 5](./05-формы-html.md)


