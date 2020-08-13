﻿# demo_test_git
-----------------------------------------------------------------------
Команды из уроков по Git
-----------------------------------------------------------------------
-c 0 урока-
git add . >Добавить все файлы
git add "index.html" > только индекс
git status > статус изменений файлов
git commit -m " тут пишем коммит "
git push > залить файлы на git
git pull > Подгружает все изменения которые были сделаны в репозиторий (с облако на комп)
git checkout --index.html > отменить действие
git reset index.html  > Удалить действия в этом файле ( или . Для того что бы во всех )
git reset --hard HEAD 1 > Удаляет действия вместе с последним коммитом (осторожно ctrl+z не работает )
git reset --soft HEAD 1 >убирает изменения, но оставляет их в файле ( не до конца понял как работает )
-до 8 урока-

-Ветки-#8 Уроки Git+GitHub - Работа с ветками git branch

git branch  > проверяет в какой мы ветке
git branch -v > последний коммит в ветке
git branch develop > создает новую ветку  названием "develop"
git checkout develop > переход в  ветку , имя "develop"
git checkout -b about (git co -b about )> создать ветку и сразу в нее перейти
git branch -m myfix > переименовываем ветку в "myfix"
git checkout e661aec > переход на  "имя e661aec" коммит
git branch -D myfix > удаляет ветку "myfix"


-----------------------------------------------------------------------
Нужно вставить  в .gitconfig для сокращения команд
-----------------------------------------------------------------------
[alias]
s = status --short
st = status
l = log --oneline --graph --decorate --all
g = log --graph --abbrev-commit --decorate --all --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%C(dim white) - %an%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n %C(white)%s%C(reset)'
br = branch
co = checkout
------------------------------------------------------------------------


-----------------------------------------------------------------------
------------Нужна когда создаем репозиторий ----------------
-----------------------------------------------------------------------
echo "# demo_test_git" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/KPATOC33/demo_test_git.git
git push -u origin master
----------------------------------------------------------------------
