# Урок 5. Формы

**Часть:** HTML  
**Результат:** `contact.html` с формой обратной связи.

## Минимум урока

- Собрать форму с `name`, `email`, `textarea`
- Связать `label` и `id` для каждого поля
- Проставить `required` там, где поле обязательно

---

## Прочитать

| № | Статья на Доке |
|---|----------------|
| 1 | [Тег `form`](https://doka.guide/html/form/) |
| 2 | [Тег `input`](https://doka.guide/html/input/) |
| 3 | [Тег `label`](https://doka.guide/html/label/) |
| 4 | [Тег `textarea`](https://doka.guide/html/textarea/) |
| 5 | [Тег `select`](https://doka.guide/html/select/) |
| 6 | [Тег `button`](https://doka.guide/html/button/) |
| 7 | [`required`](https://doka.guide/html/required/) |
| 8 | [`placeholder`](https://doka.guide/html/placeholder/) |
| 9 | [Таблицы](https://doka.guide/html/tables/) — только для данных |

---

## Главное

- `label for` = `input id` — обязательная связка (доступность).
- `placeholder` — подсказка, **не замена** label.
- Таблицы — для расписаний и данных, не для вёрстки страницы.
- Для кнопок в форме указывай `type` явно:
  - `type="submit"` — отправка формы
  - `type="button"` — обычная кнопка без отправки

**Emmet для формы:**

```
form>(label[for=name]{Имя}+input#name[type=text][required])+(label[for=email]{Email}+input#email[type=email][required])+button{Отправить}
```

Разверни и дополни `select` и `textarea`.

### Плохо / Хорошо

```html
<input type="email" placeholder="Email">

<label for="email">Email</label>
<input type="email" id="email" name="email" required>
```

---

## Практика

1. `contact.html` — та же шапка/подвал, что на главной.
2. Форма: имя, email, тема (select), сообщение, чекбокс, кнопка.
3. На главной — таблица «Расписание» (3–5 строк).

---


## Переход к следующему уроку

Переходи к уроку 6, только если:

1. Форма не отправляется при пустых обязательных полях
2. Работает переход между `index.html` и `contact.html`
3. Ты не используешь таблицу для макета страницы

---

## Проверь себя

1. Зачем `label`, если есть `placeholder`?
2. Что делает `required`?
3. Можно ли сверстать всю страницу таблицей?

---

## Самопроверка

- [ ] У каждого поля есть `label` с правильным `for`
- [ ] Навигация между страницами работает
- [ ] Таблица только для данных

**Дальше:** [Урок 6](./06-практика-html.md)


