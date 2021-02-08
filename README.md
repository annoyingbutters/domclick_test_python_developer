Тестовое задание
=================

Создать API сайта-форума на любом Python-base фрэймворке. При работе с базой данных использовать raw SQL.

API должен предоставлять методы для работы со следующими сущностями:
* Forum – форум объединяет в себе треды обсуждения различных тем (например форум посвященный обсуждению марки автомобиля)
* Thread – тред, объединяет посты (например тред содержит обсуждение конкретно модели автомобиля) и находится в форуме
* Post – содержит произвольное информационное сообщение (например сообщение пользователя с отзывом о своем авто) и относится к определенному треду
* User - пользователь, который может создавать посты

Аттрибуты сущности (могут быть расширены при реализации):

Forum
1. Название форума (уникальное)
2. Сокращенное название форума (уникальное)
3. Создатель форума

Thread
1. Название треда
2. Сокращенное название треда
3. Создатель треда
4. Дата создания
5. Информационное сообщение

Post
1. Информационное сообщение
2. Создатель сообщения
3. Дата создания

User
1. Имя пользователя
2. Email
3. Username (уникальный)


Приложение должно предоставлять следующие функционал API:

### *Базовая часть*
User
* create - создать пользователя
* updateProfile - обновить информацию о пользователе
* details - получить информацию о пользователе
* listPosts - показать все посты пользователя

Post
* create - создать пост
* details - детальная информация о посте
* list - получить список постов с фильтрацией по пользователю, треду или форуму
* remove - удалить пост
* restore - восстановить пост
* update - обновить информацию в посте

Thread
* create - создать тред
* details - детальная информация о треде
* list - список тредов с фильтрацией по форуму
* listPosts - список постов треда
* remove - удалить тред
* restore - восстановить тред

Forum
* create - создать форум
* details - детальная информация
* listThreads - получить список тредов


Формат запросов/ответов - на усмотрение автора задания.

Приложение должно быть опубликовано на https://github.com/ и должно содержать в себе
README.md как запустить приложение, docker-compose файл со всеми необходимыми для работы приложения компонентами приложения, а так же примерами как пользоваться API


### *Расширенное задание*

В дополнении к базовой части, предлагается реализовать более расширенное API

User
* follow - механизм подписки на определенного пользователя
* unfollow - отписать от пользователя
* listFollowers - список подписчиков пользователя
* listFollowing - список, на кого подписан пользователя

Thread
* subscribe - подписать пользователя на тред
* unsubscribe -  отписать пользователя от треда


Так же в дополнении к расширенному функционалу требуется реализация unit и функциональных тестов (с подготовкой тестовых данных по необходимости).
