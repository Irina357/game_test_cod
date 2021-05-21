# Этот проект создан с использованием vue.js
## Верстка без использования css фреймворков (в соответствии с ТЗ)
## Как это работает
1. При нажатии стрелки происходит пролистывание страницы к следующему блоку;
1. На третьем блоке находится фоновое видео, которое проигрывается автоматически и зацикленное;
1. Кнопка «Играть» и кнопки социальных сетей реагируют на наведение и нажатие;
## Настройка проекта
Для запуска проекта на машине разработчика используйте в консоли следующие команды:
* npm install
* npm run serve
1. В файле vue.config.je укажите название вашего репозитория на GitHab: module.exports = { publicPath: process.env.NODE_ENV === 'production' ? '/YOUR_REPO_NAME/' : '/' }
1. соберите проект, введя в консоли команду: npm run build
1. После создания папки Dist, в файле deploy.sh также укажите название вашего репозитория на GitHab: set -e
npm run build

cd dist

git init git add -A git commit -m 'deploy'

git push -f git@github.com:YOUR_USER_NAME/REPOSITORY_NAME.git master:gh-pages

cd -
Внешний вид проекта вы можете увидеть на GitHub Pages [GitHub Pages](https://irina357.github.io/game_test/)
