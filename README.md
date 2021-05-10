# Autotex Test

## Этот проект реализован с использованием следующих технологий:

1. vue.js
   1. components
   1. props
   1. пользовательские события $emit
   1. Vue Router
   1. localStorage
1. Less
   1. Less
1. Vuex    
##  Как это работает.
1. В готовый список пользователей можно добавлять объекты, удалять их, переходить к развернутому виду объекта. 
Есть поиск объектов. Для удобства тестирования предусмотрена кнопка "addListStart". С ее помощью выводится 
первоначальный список из 6 объектов и очищается localStorage. Значения, введенные пользователем между сессиями
   сохраняются в localStorage.
1. Компонент Rangeinput отзывается на движение бегунка. Первоначальное значение в него передается из глобального 
   хранилища из state через mutations.
1. Вся верстка адаптивная.   
### Настройка проекта
Для запуска проекта на машине разработчика используйте в консоли следующие команды:
* npm install
* npm run serve
### Для публикации проекта на GitHab Pages:
1. В файле vue.config.je укажите название вашего репозитория на GitHab:
`module.exports = {
    publicPath: process.env.NODE_ENV === 'production' ? '/YOUR_REPO_NAME/' : '/'
}`
1. соберите проект, введя в консоли команду:
npm run build
3. После создания папки Dist, в файле deploy.sh также укажите название вашего репозитория на GitHab:
   set -e

npm run build

cd dist

git init
git add -A
git commit -m 'deploy'

git push -f git@github.com:YOUR_USER_NAME/REPOSITORY_NAME.git master:gh-pages

cd -

#### Посмотреть данный проект вы можете на [GitHab Pages](https://irina357.github.io/autotex_test/)
[GitHab Pages](https://github.com/Irina357/autotex_test)
