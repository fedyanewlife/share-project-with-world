## Шпаргалка по Git

Привет! Эта инструкция поможет тебе разобраться в Git

---

# Репозиторий

1. Репозиторий можно создать с помощью команды `git init`
2. Первоначально файлы нужно отследить. Это можно выполнить тремя командами:
	- `git add <название_файла>` для каждого файла
	- `git add --all`, где `--all` - это флаг, указывающий на все файлы.
 	- `git add .`, где точка отвечает за всю текущую папку.
3. Текущую версию (или **коммит**) можно сохранить с помощью следующей команды:
`git commit -m '<название_коммита>'`

_Название коммита_:
* должно быть простым, чётким, ёмким;
* пояснять, что изменилось в этой версии;
* отвечать за определённый функционал.

4. Чтобы загрузить текущую версию в репозиторий, нужно воспользоваться командой `git push`.
  - предварительно нужно получить репозиторий с помощью `git remote add origin/<имя_пользователя>/<название_проекта>`
  - первая загрузка выполняется с параметрами `-u origin master`
---

# Полезные команды для работы с консолью

* `cd` (от англ. _**c**urrent **d**irectory_) - переместиться в директорию;
* `ls` - вывести содержимое папки;
* `pwd` (от англ. _**p**rint **w**orking **d**irectory_) - вывести текущую директорию;
* `touch` - создать файл
* `rm` (от англ. _**r**e**m**ove_) - удалить файл
	- папка удаляется с помощью команды `rmdir`, а создаётся — `mkdir`;
	- удалить папку со всем содержимом поможет команда `rm -r`
* `~` отвечает за ~~корневую~~ **домашнюю директорию**

---

# Хеш

У каждого коммита есть свой идентификационный номер (**хеш**).

Последняя и самая актуальная версия имеет хеш, хранящийся в файле `HEAD` в скрытой папке `.git`. Это значит, что при создании коммита этот файл постоянно обновляется.

С помощью хеша можно однозначно восстановить коммит: дату создания, автора, наименование.

# Статусы файлов

Файлы проекта могут находиться в четырёх разных состояниях:
1. `untracked` - Git не следит за данным файлом;
2. `staged` - Git начал следить за файлом, но он не попал в коммит;
3. `tracked` - данный файл успешно отслеживается;
4. `modified` - данный файл был изменён.