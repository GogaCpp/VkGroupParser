Задача:
  Создание приложения для сбора информации с сайта vk.ru
###  Описание:
Приложение представляет из себя cli-скрипт на языке python3 представлящий возможность сбора сообщений со страницы группы на сайте vk.ru за настраиваемый период.
### Условия:
1. Cli-аргументы:
  * ссылка на группу. Пример: `https://vk.com/ria`
  * начало периода (в формате `YYYY-MM-DD`)
  * путь до файла с результатами (формат: `.xlsx`)
1. Результат сбора должен представлять из себя `.xlsx` файл из трех листов:
  * Посты. Поля: post_id¹, текст, дата публикации, количество лайков, количество комментов.
  * Комментарии. Поля: post_id, user_id², текст, дата публикации.
  * Лайки. Поля: post_id, user_id²
  Посты собираются за период от значения аргумента `начало периода` и до момента начала запуска скрипта. Комментарии и лайки собираются для каждого из собранных постов без учета их времени публикации.
### Дополнительная информация
1. Для работы с Vk Api разрешается использование готовых библиотек
2. Токен для работы с Vk api присылается вместе с условием
3. Обработка ошибок не является обязательным условием, однако будет преимуществом.
##### Сноски:
1. topic_id - id поста в системе vk.ru (Для ссылки: https://vk.com/ria?w=wall-15755094_46312240 `post_id=46312240`)
2. user_id - id пользователя в системе vk.ru (Для ссылки: https://vk.com/id1 `user_id=1`)
