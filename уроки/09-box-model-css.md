# Урок 9. CSS: блочная модель

**Часть:** CSS  
**Результат:** отступы, контент по центру, аккуратная форма.

## Минимум урока

- Подключить `box-sizing: border-box`
- Ограничить ширину контента и выровнять центр
- Убрать переполнение изображений

---

## Прочитать

| № | Статья на Доке |
|---|----------------|
| 1 | [Блочная модель](https://doka.guide/css/box-model/) |
| 2 | [`padding`](https://doka.guide/css/padding/) |
| 3 | [`margin`](https://doka.guide/css/margin/) |
| 4 | [`border`](https://doka.guide/css/border/) |
| 5 | [`width`](https://doka.guide/css/width/) |
| 6 | [`box-sizing`](https://doka.guide/css/box-sizing/) |
| 7 | [`display`](https://doka.guide/css/display/) — бегло |

---

## Главное

**margin** → **border** → **padding** → **content**.

```css
main {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 16px;
}

img {
  max-width: 100%;
  height: auto;
}
```

**Emmet:** `p16` + Tab, `m0a` + Tab, `bdb1#e5e5e5` + Tab для линии под шапкой.

---

## Практика

1. `main` по центру, отступы между секциями.
2. Шапка с `border-bottom` или фоном.
3. Поля формы: ширина 100%, padding, рамка.

### Дополнительно

Лёгкая тень у карточки (пригодится в уроке 10):

```css
.card {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}
```

---


## Переход к следующему уроку

Переходи к уроку 10, только если:

1. Применен `box-sizing: border-box`
2. Понимаешь разницу между `margin` и `padding`
3. Нет горизонтального скролла из-за картинок

---

## Проверь себя

1. Чем padding отличается от margin?
2. Зачем `box-sizing: border-box`?
3. Что делает `margin: 0 auto` у блока с `max-width`?

---

## Самопроверка

- [ ] Нет горизонтального скролла из-за картинки
- [ ] Форма аккуратная
- [ ] main ограничен по ширине

**Дальше:** [Урок 10](./10-flexbox-css.md)


