# Spline
## Инструкция по установке для разработчиков
P.S. Пользователям Windows, чтобы сильно не страдать, рекомендую поставить **WSL2** и **Windows Terminal**.

### Установка всех необходимых зависимостей

Debain-based:
```bash
sudo apt-get install git cmake glm doxygen gcc make
```
Arch-based:
```bash
sudo pacman -S git cmake glm doxygen gcc make
```

### Скачивание репозитория
```bash
git clone https://github.com/KMBO-01-19-Spline/spline.git
```
ну и для фанатов SSH:
```bash
git clone git@github.com:KMBO-01-19-Spline/spline.git
```

### Компиляция
Загружаем библиотеку
```bash
git submodule init
git submodule update
```
Команду выполнять из корневой папки проекта
```bash
cmake -S . -B build && cmake --build build
```

### А прогать как?
Для написания кода используете следующие файлы:
* apps/app.cpp - main()
* src/* - реализация Integral и Diff
* include/spline/* - интерфейс Integral и Diff

Все необходимое для работы уже подключено.

### Самая маленькая инструкция по работе с GitHub
Когда написали код и хотите залить его на сервер, нужно выполнить след.действия

#### Первоначальная настройка git
```bash
git config --global user.name "My Name"
git config --global user.email myEmail@example.com
```

#### Посмотреть изменения, которые вы сделали:
```bash
git status
```
#### Сохраняем изменения

А теперь внимательно. Заливать изменения на основную ветку НЕНУЖНО. Вы создаете отдельную ветку и вносите изменения туда, потом она будет соединена с основной веткой. 

Создаем ветку
```bash
git branch your_branch
```
Переключаемся на нее
```bash
git checkout your_branch
```

Добавить изменения для коммита (что-то вроде блока изменений):
```bash
git add имя_файла
```

Создать коммит:
```bash
git commit -m "Ваше описание изменений"
```

Заливаем на новую ветку
```bash
git push https://github.com/KMBO-01-19-Spline/spline.git your_branch

```
Для SSH:

```bash
git git@github.com:KMBO-01-19-Spline/spline.git push your_branch
``` 
#### Не забываем получать обновления с сервера 

Эта команда вызывает слияния. Проблем быть не должно, если вы сразу коммите в новую ветку
```bash
git pull
```

Эта команда без слияний. Сохраняет изменения в **refs/remotes/**
```bash

git fetch

```
### Документация
Пишите комментарии ко всему коду, там видно будет. В doxygen, кстати, есть поддержка LaTeX, так что можно будет вставлять формулы, когда будет теория

