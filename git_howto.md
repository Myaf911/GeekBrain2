# git команды для терминала

## Команда смены директории
```sh
cd ~
```

## Команда для отображения текущей директории MacOS, Linux
```sh
pwd
```

## Листинг текущей директории (узнать текущую директорию)

### for Win
```sh
dir
```
### for Mac
```sh
ls
```

## Удалить файл
### for Win
```sh
del <file_name>
```

### for MacOS, Linux
```sh
rm <file_name>
```

## Инициализировать Git через терминал в нужной папке
```sh
git init 
```

## Что-бы добавить файл для отслеживания

```sh
git add <file_name>
```

## Добавить комментарий (чекпоинт) к сохраненной версии

```sh
git commit -m "<text>"
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git commit -m "was born"
[main b358559] was born
 1 file changed, 1 insertion(+)
 create mode 100644 git_howto.md
```

## Посмотреть лог изменений 
```sh
git log
```

Ответ терминала
```sh
commit 407cc63a5166fc9b3d6f0e112532372054fab04e (HEAD -> master)
Author: Ilya <ilyakatasonov@gmail.com>
Date:   Mon Nov 14 02:15:40 2022 +0300
Date:   Mon Nov 14 02:15:40 2022 +0300

    git add and git commit -m  add

commit a08ebb35e6f0e72c6e93d73e00ef7ccc354ec81b
Author: Ilya <ilyakatasonov@gmail.com>
Date:   Mon Nov 14 02:14:26 2022 +0300

    git init add

commit 4cb21c7e359a11b8210e91648b80b3e7322111a7 (origin/master)
Author: Ilya <ilyakatasonov@gmail.com>
Date:   Mon Nov 14 02:12:49 2022 +0300

    Head 1 lvl add

commit 8ab2b7713ba5d4979f321db7da8c659a4e5d5f28
Author: Ilya <ilyakatasonov@gmail.com>
Date:   Mon Nov 14 02:06:37 2022 +0300
Date:   Mon Nov 14 02:06:37 2022 +0300

    was born
```

## Посмотреть логи изменений в одну строку

```sh
git log --oneline
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain % git log --oneline
ddf3b3c (HEAD -> master, origin/master) git checkout add
d044bcf git log and git --oneline add
407cc63 git add and git commit -m  add
a08ebb3 git init add
4cb21c7 Head 1 lvl add
8ab2b77 was born
```

## Откатить папку к нужному комментарию
```sh
git checkout <номер нужного комментария>
```

Ответ терминала

## Посмотреть дерево изменений с учетом всех веток
```sh
git log –graph
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git log --graph
*   commit 49c369af58895ffa6c6be617c2841c136cf69e34 (HEAD -> master)
|\  Merge: 3c07d6c 0b3ee6b
| | Author: Ilya <ilyakatasonov@gmail.com>
| | Date:   Mon Nov 14 10:25:25 2022 +0300
| | 
| |     Смерджили изменения с учетом конфликтов в ветке images
| | 
| * commit 0b3ee6b86201a5aec03baa922cc38620e747e781 (lists)
| | Author: Ilya <ilyakatasonov@gmail.com>
| | Date:   Mon Nov 14 09:44:30 2022 +0300
| | 
| |     lists added
| | 
* | commit 15aa484af7e9072e8509414608609b9e343a4980
|/  Author: Ilya <ilyakatasonov@gmail.com>
|   Date:   Mon Nov 14 09:32:13 2022 +0300
| 
|     Was Born
| 
* | commit aca3c09fa4f472ea69033b4f9095ac5c48a8eafa
|/  Author: Ilya <ilyakatasonov@gmail.com>
| Date:   Mon Nov 14 09:00:39 2022 +0300
```
## Откатить вилку к нужному комментарию
```sh
git checkout <номер нужного комментария>
```

## Откатить вилку на основную ветку
```sh
git checkout master
```

## Показать текущие изменения если файл еще не добавлен
```sh
git diff
```
 
## Сбросить все изменения в еще не добавленом файле. Удалится без возвратно
```sh
git restore <file_name>
```

## Посмотреть в чем отличаются комментарии между собой
```sh
git diff <номер нужного комментария> <номер нужного комментария>
```

## Работа с ветками
```sh
git branch
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git branch
* master
```
## Создать новую ветку
```sh
git branch <branch_name>
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git branch txt_formatting
После добавления, если повторить команду git branch то

myaf@MacBook-Pro-Katasonov GeekBrain2 % git branch
* master
  txt_formatting
```

## Что бы сменить выбранную ветку:
```sh
git checkout <branch_name>
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git checkout txt_formatting
Switched to branch 'txt_formatting'
```

## Слияние веток
```sh
git merge <branch_name>
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git merge txt_formatting
Updating 29a7df3..1b9ce05
Fast-forward
 MD_inst.md | 7 +++++++
 1 file changed, 7 insertions(+)
myaf@MacBook-Pro-Katasonov GeekBrain2 % 
```

## Удаление веток
```sh
git branch -d <branch_to_delete>
```

Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git branch -d txt_formatting  
Deleted branch txt_formatting (was 1b9ce05).
```

## Клонируем чужой внешний репозиторий
Эта команда позволяет склонировать внешний репозиторий на наш ПК 

```sh
git clone <url>
```

## Скачать и смерджить с нашей локальной версией
Эта команда позволяет скачать все из текущего репозитория и автоматически
сделать merge с нашей версией 
```sh
git pull
```

## Отправляем локальный репозиторий на внешний репозиторий
эта команда позволяет отправить нашу версию репозитория на внешний
репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ на внешнем репозитории 
```sh
git push
```
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git push
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.88 KiB | 1.88 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Myaf911/GeekBrain2.git
   b584b2a..c8bc6d5  main -> main
```

Я закидывал к себе второе практическое задание
```sh
git push -u origin main
```
Ответ терминала
```sh
myaf@MacBook-Pro-Katasonov GeekBrain2 % git push
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 2.32 KiB | 2.32 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Myaf911/GeekBrain2.git
   beb5da4..b584b2a  main -> main
```

## Как сделать pull request
Делаем fork репозитория
● Делаем clone СВОЕЙ версии репозитория
● Создаем новую ветку и в НЕЕ вносим свои изменения
● Фиксируем изменения (делаем коммиты)
● Отправляем свою версию в свой GitHub
● На сайте GitHub нажимаем кнопку pull request 

## Работаем с репозиториями

```sh
git remote add origin <URL>
```
>Это добавляет новый удаленный сервер гитхаба в список серверов куда мы можем пушить. **Origin** это название сервера. Обычно оно стандартное хотя вы можете выбрать любое имя.

То что он у нас добавился мы можем посмотреть командой
```sh
git remote -v
```
>И оно нам выводит репозиторий, который мы добавили.

Теперь нужно подружить локальный Git и GitHub
```sh
git push -u origin master
```
>При первм входе в репозиторий оно запрашивает логин и пароль. Вводим оба. Видим сообщение, что данные были записаны в нашу репу на GitHub.

## Отмена внесенных изменений
Если внесли изменения и нужно быстро их отменить, то воспользуйтесь командой git reset, которая отменяет все незафиксированные изменения.
```sh
git reset
```
> Она отменяет все незафиксированные изменения.

Жесткая отмена изменений из локального репозитория и индеса
```sh
git reset --hard
```
>Безвозвратно удаляет незафиксированные текущие изменения!

## После окончания работы
```sh
git clean -f -d
```
>После работы в репозитории могут оставаться различные ненужные, неотслеживаемые файлы и прочий мусор. Чтобы удалить всё лишнее.