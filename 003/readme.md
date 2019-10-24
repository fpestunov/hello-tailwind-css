# Lab #3. Setting up Tailwind and PostCSS

Learn how to install Tailwind and get it compiling in a simple HTML project.

https://tailwindcss.com/course/setting-up-tailwind-and-postcss

1. Установка Tailwind

```
npm init -y
clear
npm install tailwindcss postcss-cli autoprefixer
```

2. Теперь будем конфигурировать Tailwind

```
npx tailwind init
```

> Хммм. Почему то не заработало :((
> А когда в корне создаю, то все работает!

Создаем файл `postcss.config.js` и пропишем плагины, кт будем использовать.

```
module.exports = {
  plugins: [
    require('tailwindcss'),
    require('autoprefixer'),
  ]
}
```

> Почему то не работает Tailwind Intellisense :(

Далее создаем файл `css\tailwind.css` и прописываем содержимое.

Теперь сделаем скрипт, который будет прогонять этот файл через PostCSS.

Запускаем сборку - `npm run build`
Создадим `index.html` и начнем писать код. Отлаживаем через `live-server имя-папки` (`npm install -g live-server`)

```
live-server public
```