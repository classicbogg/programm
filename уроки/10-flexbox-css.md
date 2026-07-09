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
- **Emmet CSS:** `df` + Tab, `jcsb` + Tab, `aic` + Tab, `g20` + Tab.

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

**Emmet HTML:** `article.card>.card__badge{Новое}+h3+p`

---

## Практика

1. Flex-шапка: логотип слева, меню справа.
2. Hero по центру (`flex-direction: column`, `align-items: center`).
3. Три карточки в `section`.
4. Бейдж на одной карточке через `position`.

### По желанию

[Flexbox Froggy](https://flexboxfroggy.com/#ru)

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


