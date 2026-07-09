# CSS шпаргалка для начинающих (расширенная)

Эта шпаргалка помогает быстро вспомнить синтаксис и основные свойства.  
Подробный справочник: [Doka CSS](https://doka.guide/css/).

---

## 1) Как выглядит CSS-правило

```css
селектор {
  свойство: значение;
}
```

Пример:

```css
h1 {
  color: #111827;
  font-size: 2rem;
}
```

---

## 2) Способы подключения CSS

1. Внешний файл (лучший вариант):

```html
<link rel="stylesheet" href="css/styles.css">
```

2. Встроенный `<style>` (для быстрых прототипов)
3. Inline `style=""` (почти не использовать)

---

## 3) Селекторы — база

| Селектор | Что выбирает |
|----------|--------------|
| `p` | все `<p>` |
| `.card` | элементы с классом `card` |
| `#hero` | элемент с id `hero` |
| `nav a` | ссылки внутри `nav` |
| `.card h3` | `h3` внутри `.card` |
| `h1, h2` | перечисление селекторов |
| `.card:hover` | состояние наведения |
| `input:focus` | состояние фокуса |

---

## 4) Каскад и приоритет (очень важно)

- Более **точный** селектор обычно приоритетнее
- Стиль ниже в файле часто перекрывает стиль выше
- `!important` использовать только в крайних случаях

Практика:
предпочитай классы и понятные правила вместо сложных “магических” селекторов.

---

## 5) Единицы измерения

| Единица | Когда использовать |
|---------|--------------------|
| `px` | границы, мелкие отступы |
| `%` | относительная ширина |
| `rem` | шрифты, основные отступы |
| `em` | относительно текущего шрифта |
| `vw`, `vh` | размеры от окна браузера |

---

## 6) Блочная модель (Box Model)

Порядок: `margin -> border -> padding -> content`.

```css
* {
  box-sizing: border-box;
}

.card {
  width: 300px;
  padding: 16px;
  border: 1px solid #d1d5db;
  margin: 16px;
}
```

---

## 7) Текст и типографика

| Свойство | Пример |
|----------|--------|
| `font-family` | `system-ui, sans-serif` |
| `font-size` | `16px`, `1rem`, `2rem` |
| `font-weight` | `400`, `500`, `700` |
| `line-height` | `1.5`, `1.6` |
| `letter-spacing` | `0.02em` |
| `text-align` | `left`, `center` |
| `text-decoration` | `none`, `underline` |

---

## 8) Цвет и фон

| Свойство | Пример |
|----------|--------|
| `color` | цвет текста |
| `background-color` | цвет фона |
| `background` | короткая запись фона |
| `opacity` | прозрачность |

Форматы цвета:
`#2563eb`, `rgb(37, 99, 235)`, `hsl(...)`.

---

## 9) Display и поток

| Значение | Поведение |
|----------|-----------|
| `block` | с новой строки, занимает ширину |
| `inline` | в строке, без width/height |
| `inline-block` | в строке, но с размерами |
| `none` | скрыть элемент |
| `flex` | flex-контейнер |
| `grid` | сетка (следующий этап) |

---

## 10) Flexbox — самый нужный в курсе

```css
.row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
}

.item {
  flex: 1 1 280px;
}
```

Главные свойства:
`display: flex`, `flex-direction`, `justify-content`, `align-items`, `gap`, `flex-wrap`, `flex`.

---

## 11) Position (база)

| Значение | Что делает |
|----------|-------------|
| `static` | по умолчанию |
| `relative` | базовая точка для absolute |
| `absolute` | позиционирование относительно ближайшего relative |
| `fixed` | фиксирован к окну браузера |
| `sticky` | “прилипает” при скролле |

Пример бейджа:

```css
.card { position: relative; }
.badge { position: absolute; top: 8px; right: 8px; }
```

---

## 12) Псевдоклассы и псевдоэлементы

Псевдоклассы:
`:hover`, `:focus`, `:active`, `:visited`, `:first-child`, `:last-child`, `:nth-child(n)`.

Псевдоэлементы:
`::before`, `::after`, `::placeholder`, `::selection`.

Пример:

```css
a:hover { color: #1d4ed8; }
a:focus { outline: 2px solid #2563eb; }
```

---

## 13) Формы и кнопки

```css
label {
  display: block;
  margin-bottom: 6px;
}

input,
textarea,
select {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid #d1d5db;
  border-radius: 6px;
}

button {
  padding: 10px 18px;
  border: none;
  border-radius: 6px;
  background: #2563eb;
  color: #fff;
  cursor: pointer;
}
```

---

## 14) Адаптивность и media queries

Подход: **mobile first**.

```css
.nav {
  display: flex;
  flex-direction: column;
}

@media (min-width: 768px) {
  .nav {
    flex-direction: row;
  }
}
```

Проверяй как минимум: `320px`, `768px`, `1200px`.

---

## 15) CSS-переменные (custom properties)

```css
:root {
  --color-primary: #2563eb;
  --color-text: #1f2937;
  --radius: 8px;
}

body {
  color: var(--color-text);
}

.btn {
  background: var(--color-primary);
  border-radius: var(--radius);
}
```

---

## 16) Переходы и простая анимация

```css
.card {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
}
```

---

## 17) Частые ошибки новичков

1. CSS-файл не подключен или неверный путь  
2. Путают `margin` и `padding`  
3. Ставят `display: flex` не на родителя  
4. Используют фиксированную ширину и ломают мобильную версию  
5. Используют имена классов типа `.div1`, `.block2`

---

## 18) Быстрые рабочие сниппеты

### Центрирование контейнера

```css
.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 16px;
}
```

### Сетка карточек (Flex)

```css
.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 280px;
}
```

### Безопасные изображения

```css
img {
  max-width: 100%;
  height: auto;
  display: block;
}
```

---

## 19) Emmet для CSS (ускорение)

| Сокращение | Результат |
|------------|-----------|
| `df` | `display: flex;` |
| `jcsb` | `justify-content: space-between;` |
| `jcc` | `justify-content: center;` |
| `aic` | `align-items: center;` |
| `fdc` | `flex-direction: column;` |
| `fww` | `flex-wrap: wrap;` |
| `g20` | `gap: 20px;` |
| `m0a` | `margin: 0 auto;` |
| `w100p` | `width: 100%;` |
| `bsbb` | `box-sizing: border-box;` |

---

## 20) Минимум, который нужно уметь к концу курса

- Подключить внешний CSS
- Стилизовать текст, фон, ссылки, кнопки
- Собрать шапку и карточки на Flexbox
- Сделать адаптив через `@media`
- Применять переменные и базовый `:focus`


