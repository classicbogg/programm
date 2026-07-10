# Урок 10. CSS: Flexbox и position

**Часть:** CSS  
**Результат:** меню, hero, карточки; базовый `position` для бейджа.

## Минимум урока

- Собрать шапку через Flexbox
- Сделать блок карточек с переносом
- Понять связку `relative` + `absolute`

---

## Прочитать

| № | Статья на Доке |
|---|----------------|
| 1 | [**Гайд по Flexbox**](https://doka.guide/css/flexbox-guide/) |
| 2 | [Свойство flex-direction](https://doka.guide/css/flex-direction/) |
| 3 | [Свойство justify-content](https://doka.guide/css/justify-content/) |
| 4 | [Свойство align-items](https://doka.guide/css/align-items/) |
| 5 | [Свойство gap](https://doka.guide/css/gap/) |
| 6 | [Свойство flex-wrap](https://doka.guide/css/flex-wrap/) |
| 7 | [Свойство position](https://doka.guide/css/position/) — разделы про `relative` и `absolute` |

---

## Главное — Flexbox

- `display: flex` на **родителе**.
- `justify-content` — главная ось; `align-items` — поперечная.
- **CSS:** свойства Flexbox пиши обычным текстом (`display: flex`, `justify-content`, `align-items`, `gap`).

**Важно различать:**
- **Flexbox** — это контейнер через `display: flex` на родителе.
- **`flex: 1 1 280px`** — отдельное свойство у карточки; поначалу можно просто копировать из примера.

```css
.header-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 280px;
  padding: 24px;
}
```

### position — минимум

Чтобы повесить бейдж «Новое» на угол карточки:

```css
.card {
  position: relative;
}

.card__badge {
  position: absolute;
  top: 12px;
  right: 12px;
}
```

Родитель с `relative`, элемент с `absolute` — относительно родителя.

**Emmet HTML:** вставь `article` → Tab, внутри `h3` → Tab и `p` → Tab; для бейджа — `div` → Tab внутри карточки.

---

## Практика

Все задания — в файле [урок-10-практика.md](../практика/урок-10-практика.md).
Выполняй по порядку: **База → Средний → Продвинутый**.


## Типичные ошибки урока

1. `display: flex` на карточке, а не на родителе — flex работает только на контейнере.
2. Карточки не переносятся — добавь `flex-wrap: wrap` и `gap`.
3. Бейдж уехал не туда — у карточки должен быть `position: relative`, у бейджа `absolute`.

---

## Переход к следующему уроку

Переходи к уроку 11, только если:

1. Ты знаешь, на какой элемент ставится `display: flex`
2. Карточки переносятся при сужении окна
3. Понимаешь связку `relative` + `absolute`

---

## Проверь себя

1. На каком элементе нужен `display: flex`?
2. Чем `space-between` отличается от `center`?
3. Зачем карточке `position: relative` для бейджа?

---

## Самопроверка

- [ ] Меню в ряд на широком экране
- [ ] 3 карточки с переносом
- [ ] Понимаешь связку relative + absolute

**Дальше:** [Урок 11](./11-адаптив-css.md)


