# Foundation for Emails Template

[![devDependency Status](https://david-dm.org/ncer/foundation-emails-template/dev-status.svg)](https://david-dm.org/ncer/foundation-emails-template#info=devDependencies)

Установка [описана в исходном репозитории](https://github.com/zurb/foundation-emails-template).

## Быстрые подсказки по верстке

### Блок ограниченной ширины по центру экрана

```html
<container></container>
```

### Блок на всю ширину экрана

```html
<wrapper></wrapper>
```

### Схлопнутый блок (без внутренних отступов)

```html
<container>
  <row class="collapse"></row>
</container>
```

### Колонки

```html
<container>
  <row class="collapse">
    <columns small="12" large="4"></columns>
    <columns small="12" large="4"></columns>
    <columns small="12" large="4"></columns>
  </row>
</container>
```

Примечение: при использовании колонок, блок рекомендуется всегда делать схлопнутым `<row class="collapse">`, т.к. на некоторых клиентах (напр., android-клиент Mail.ru) верстка может поехать.

### Вертикальный отступ

```html
<spacer size="100"></spacer>
```

Создаст таблицу высотой 100px - железобетонный вариант, работающий везде (даже в Outlook).

### Кнопка

```html
<button href="">Button</button>
```

Создаст ссылку в таблице - железобетонный вариант, работающий везде (даже в Outlook).

Больше примеров в [официальной документации](https://foundation.zurb.com/emails/docs/).

## Особенности почтовых клиентов

### Yandex

Android-клиент выпиливыает Media Queries (точнее тег `<style>`, в котором они лежат) и просто масштабирует десктопную версию письма. Поэтому использовать `min-width` нельзя! А `max-width` - можно, т.к. его поймут те, кто их поддерживает (напр., Gmail).

### Mail.ru

На android-клиенте едет верстка, если колонки имеют горизонтальные паддинги. Поэтому всегда нужно их убирать с помощью `<row class="collapse">`.