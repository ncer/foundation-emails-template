# Foundation for Emails Template

[![devDependency Status](https://david-dm.org/zurb/foundation-emails-template/dev-status.svg)](https://david-dm.org/zurb/foundation-emails-template#info=devDependencies)

Установка [описана в исходном репозитории](https://github.com/zurb/foundation-emails-template).

## Особенности почтовых клиентов

### Yandex

Android-клиент выпиливыает Media Queries и просто масштабирует десктопную версию письма. Поэтому использовать `min-width` нельзя! А `max-width` - можно, т.к. его поймут те, кто их поддерживает (Gmail).

### Mail.ru

Android-клиент не отображает самую нижнюю картинку. Решение: 
1. В Media Queries (т.к. это фактически мобильная версия) для картинки добавить `min-height` 
1. Добавить небольшой `<spacer>` в конец письма