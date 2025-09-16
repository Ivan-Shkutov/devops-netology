## Домашнее задание к занятию «Основы Git»

### Задание 1. Знакомимся с GitLab и Bitbucket

### GitLab

Создадим аккаунт в GitLab, если у вас его ещё нет:

1. GitLab. Для регистрации можно использовать аккаунт Google, GitHub и другие.
   
2. После регистрации или авторизации в GitLab создайте новый проект, нажав на ссылку Create a projet. Желательно назвать также, как и в GitHub — devops-netology и visibility level, выбрать Public.

3. Галочку Initialize repository with a README лучше не ставить, чтобы не пришлось разрешать конфликты.

![1](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/1.png)

![2](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/2.png)

![3](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/3.png)

4. Если вы зарегистрировались при помощи аккаунта в другой системе и не указали пароль, то увидите сообщение: You won't be able to pull or push project code via HTTPS until you set a password on your account. Тогда перейдите по ссылке из этого сообщения и задайте пароль. Если вы уже умеете пользоваться SSH-ключами, то воспользуйтесь этой возможностью (подробнее про SSH мы поговорим в следующем учебном блоке).

5. Перейдите на страницу созданного вами репозитория, URL будет примерно такой: https://gitlab.com/YOUR_LOGIN/devops-netology. Изучите предлагаемые варианты для начала работы в репозитории в секции Command line instructions.

6. Запомните вывод команды git remote -v.

7. Из-за того, что это будет наш дополнительный репозиторий, ни один вариант из перечисленных в инструкции (на странице вновь созданного репозитория) нам не подходит. Поэтому добавляем этот репозиторий, как дополнительный remote, к созданному репозиторию в рамках предыдущего домашнего задания: git remote add gitlab https://gitlab.com/YOUR_LOGIN/devops-netology.git.

8. Отправьте изменения в новый удалённый репозиторий git push -u gitlab main.

9. Обратите внимание, как изменился результат работы команды git remote -v.

![4](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/4.png)

### Задание 2. Теги

Представьте ситуацию, когда в коде была обнаружена ошибка — надо вернуться на предыдущую версию кода, исправить её и выложить исправленный код в продакшн. Мы никуда не будем выкладывать код, но пометим некоторые коммиты тегами и создадим от них ветки.

1. Создайте легковестный тег v0.0 на HEAD-коммите и запуште его во все три добавленных на предыдущем этапе upstream.

2. Аналогично создайте аннотированный тег v0.1.

![5](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/5.png)

3. Перейдите на страницу просмотра тегов в GitHab (и в других репозиториях) и посмотрите, чем отличаются созданные теги.

в GitHub — https://github.com/YOUR_ACCOUNT/devops-netology/releases;

в GitLab — https://gitlab.com/YOUR_ACCOUNT/devops-netology/-/tags;

![6](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/6.png)


### Задание 3. Ветки

Давайте посмотрим, как будет выглядеть история коммитов при создании веток.

1. Переключитесь обратно на ветку main, которая должна быть связана с веткой main репозитория на github.

2. Посмотрите лог коммитов и найдите хеш коммита с названием Prepare to delete and move, который был создан в пределах предыдущего домашнего задания.

3. Выполните git checkout по хешу найденного коммита.

4. Создайте новую ветку fix, базируясь на этом коммите git switch -c fix.

5. Отправьте новую ветку в репозиторий на GitHub git push -u origin fix.

![7](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/7.png)

6. Посмотрите, как визуально выглядит ваша схема коммитов: https://github.com/YOUR_ACCOUNT/devops-netology/network.

![8](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/8.png)

![9](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/9.png)

![10](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/10.png)

7. Теперь измените содержание файла README.md, добавив новую строчку.

8. Отправьте изменения в репозиторий и посмотрите, как изменится схема на странице https://github.com/YOUR_ACCOUNT/devops-netology/network и как изменится вывод команды git log.

![11](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/11.png)

![12](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/12.png)

![13](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/13.png)

![14](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/14.png)

### Задание 4. Упрощаем себе жизнь

Попробуем поработь с Git при помощи визуального редактора.

1. В используемой IDE PyCharm откройте визуальный редактор работы с Git, находящийся в меню View -> Tool Windows -> Git.

2. Измените какой-нибудь файл, и он сразу появится на вкладке Local Changes, отсюда можно выполнить коммит, нажав на кнопку внизу этого диалога.

3. Элементы управления для работы с Git будут выглядеть примерно так:

4. Попробуйте выполнить пару коммитов, используя IDE.

![15](https://github.com/Ivan-Shkutov/devops-netology/blob/fix/15.png)

Если вверху экрана выбрать свою операционную систему, можно посмотреть горячие клавиши для работы с Git. Подробней о визуальном интерфейсе мы расскажем на одной из следующих лекций.

В качестве результата работы по всем заданиям приложите ссылки на ваши репозитории в GitHub, GitLab и Bitbucket.
