University: [ITMO University](https://itmo.ru/ru/)<br>
Faculty: [FTMI](https://ftmi.itmo.ru/)<br>
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)<br>
Year: 2025/2026<br>
Group: U4125<br>
Author: Shishkina Sofya Anatolievna<br>
Lab: Lab0<br>
Date of create: 08.09.2026<br>
Date of finished:<br>

# Лабораторная работа №0

1. Создан аккаунт на GitHub и настроены SSH ключи для работы с репозиториями:
	1. Зарегистрирован аккаунт на почту "sofyashishkina2003@gmail.com".
	2. С [сайта](https://git-scm.com/install/) скачан Git.
	3. Созданы ssh-ключи. Для этого выполнены PowerShell-команда `ssh-keygen -t ed25519 -C "sofyashishkina2003@gmail.com"`
	4. В настройках аккаунта GitHub добавлен публичный ssh-ключ.
2. Создан новый репозиторий - 2026_2027-introduction-in-web-tech-U4125-shishkina_s_a
3. С помощью `git clone` репозиторий склонирован.
4. Создан файл README.md с описанием проекта, вашими контактными данными и планом изучения DevOps.
5. Создан файл .gitignore, в котором описаны игнорируемые git'ом файлы - *.test. Для примера создан файл ignored.test, который позже НЕ будет загружен на удалённый репозиторий.
6. Создана ветка develop: `git checkout -b develop`, на которую сразу же переключились.
7. Создан файл CONTRIBUTING.md с описанием участия в проекте.
8. Создан коммит с текстом "docs: первичное описание проекта" и изменения отправлены на удалённый репозиторий:
	1. `git add -A` - добавить все файлы в коммит.
	2. `git status` - посмотреть статус коммита (увидим, что создано и модифицировано несколько файлов).
	3. `git commit -m"docs: первичное описание проекта"` - попытка создания коммита. Создать не получилось, т.к. нужно настроить данные пользователя (ниже).
	4. Для создания коммита выполнены команды `git config --global user.name "sofyashishkina"`  
`git config --global user.email "sofyashishkina2003@gmail.com"`.
	5. `git commit -m"docs: первичное описание проекта"` - коммит создан.
	6. `git push` - попытка отправки на удалённый репозиторий. Не сработало, т.к. нужно ввести `git push --set-upstream origin develop`.
	7. `git push --set-upstream origin develop` - коммит запушен.
9. На GitHub через появившееся окно создан Pull Request.
10. Pull Request слит в интерфейсе GitHub, а ветка `develop` удалена. Для этого:
	1. `git branch main` - переключиться на ветку `main`.
	2. `git pull` - синхронизировать локальный репозиторий с удалённым.
	3. `git branch -d develop` - удалить локальную ветку `develop`.
	4. `git push origin --delete develop` - удалить ветку `develop` на удалённом репозитории.