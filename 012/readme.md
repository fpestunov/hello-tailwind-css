# Structuring a Basic Card
https://tailwindcss.com/course/structuring-a-basic-card

install Vue Highlight https://github.com/vuejs/vue-syntax-highlight/tree/new

Learn how to use Tailwind's utility classes to structure a basic card component.

1) В файле `App.vue` написали основной компонент и подключили PropertyCard;
2) Добавили файл `PropertyCard` и создали пустой шаблон;

Начинаем:
- делаем структуру для `PropertyCard`;
- добавляем классы оформления;

## Making Text Content Feel Designed

- если малозаметный текст вынести за другой, то это выглядет аккуратнее!
- а если заголовок будет длиннее? надо добавить Марджины и обрезать лишнее `truncate`;

## Working with SVG Icons

Learn how to incorporate and style SVG icons in a Tailwind project.

Как использовать?
https://tailwindcss.com/resources#icons

Оптимизация СВГ:
https://jakearchibald.github.io/svgomg/

- берем иконку, оптимизируем и вставляем в наш код;
- убираем у СВГ размеры, тк будем управлять ими через класс;
- добавляем вывод в цикле и делаем через флекс;

## Designing a Badge
Learn how to build and style a simple badge component.

## Cropping and Positioning Images
Learn how to fit an image into a specific size without distorting it.

```
img class="..."
object-left
object-right
object-top
object-cover
```

Почему реализация через див предпочтительнее?

Нет, он сказал делать через тэг ИМГ, т.к. это доступнее для пользователей.
