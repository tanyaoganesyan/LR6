# LR6
Лабораторная работа №6

Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git API, опыт работы с локальным и удаленным репозиторием.

Выполнение работы

* Сделать fork репозитория на GitHub
![делать fork репозитория на GitHub](screens/screen-02.png)

* Клонировать свой личный удалённый репозиторий на компьютер.
![Клонировать свой личный удалённый репозиторий на компьютер](screens/screen-01.png)
```bash
git clone https://github.com/tanyaoganesyan/LR6.git
```

 * Добавить файл через интерфейс GitHub. Подтянуть изменения в локальный репозиторий.
![Добавить файл через интерфейс GitHub. Подтянуть изменения в локальный репозиторий](screens/screen-03.png)
```bash
git pull
```

*  Получить историю операций для каждой из веток.
![code](screens/screen-04.png)
```bash
git log --graph
```

* Просмотреть последние изменения. 
![Получить историю операций для каждой из веток](screens/screen-05.png)
```bash
git log
```

* Выполнить слияние в ветку master, разрешив конфликт.
![Выполнить слияние в ветку master, разрешив конфликт](screens/screen-06.png)
```bash
git branch test-branch
git checkout test-branch
git add .
git commit -m "file changed in test-branch"
git checkout master
git merge test-branch
```

* Удалить побочную ветку после успешного слияния.
![Удалить побочную ветку после успешного слияния](screens/screen-07.png)
```bash
git branch -d test-branch
```

* Сделать изменения и зафиксировать их, оставляя комментарии ,несколько раз. 
![Сделать изменения и зафиксировать их, оставляя комментарии ,несколько раз](screens/screen-08.png)
```bash
git add . 
git commit -m "file changed after merging from master"
```

* Сделать откат коммита. 
![Сделать откат коммита](screens/screen-09.png)
```bash
git reset --soft HEAD~1
git log
```

* Создать ветку для отчёта.

Поступим по аналогии с действиями в начале работы:
```bash
git branch report
git checkout report
```


* Начать оформлять отчёт.

* Получить историю операций в форматированном виде.
![Получить историю операций в форматированном виде](screens/screen-10.png)
* Отправить локальные изменения в сетевое хранилище GitHub

```bash
git log --pretty=format:"%h %ad %an %s"
```
* Отправить локальные изменения в сетевое хранилище GitHub
![Отправить локальные изменения в сетевое хранилище GitHub](screens/screen-11.png)
```bash
git push -u origin 
```
