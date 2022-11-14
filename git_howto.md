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


