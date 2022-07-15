# Инструкция по работе с Git

## Что такое git?
Git  - это одна из реализаций распределенных систем контроля версий, что позволяют иметь версионность как в локальном репозитории(общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда "git init". В терминале в папке с будущим репозиторием достаточно написать "git init", и эта папка станет репозиторием.

## Создание "commits"

###  Добавление файла в "commit"
Для добавления файла в текущий коммит используется команда "git add". Для этого достаточно в терминале с папкой текущего репозитория написать "git add" *<название файла>*.

### Сохранение Commit
Для сохранения Commit используется комманда *"git commit"*. Для этого в терминале с папкой репозитория необходимо написать команду *git commit -m "<сообщение к коммиту>*. Сообщение к коммиту писать *** ОБЯЗАТЕЛЬНО***.

## Перемещение между "commits"
Для перемещения между коммитами необходимо использовать команду *" git checkout. Для этого в терминале с папкой репозитория  необходимо написать *"git checkout <номер коммита>*. Номер коммита берется из истории изменений. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обратное состояние используется команда *<git checkout master>*.

## Журнал изменений
Для просмотра историй коммитов, используется комманда *<git log>*. Для этого необходимо в терминале с папкой-репозиторием написать *git log*.

## Создание веток 
Ветки в GIT – представляют собой указатель на снимок изменений, - коммит. 
Если нужно добавить новую возможность или исправить ошибку (незначительную или серьезную), создается  новая ветка, в которой будут размещаться эти изменения.
Для того, чтобы создать ветку необходимо воспользоваться командой *“git branch”*  имя ветки.

## Слияние веток 
Процедура объединения веток называется слияние (merge). Для слияния текущей ветки с какой-либо другой используется команда “git merge” имя_ветки. В результате выполнения этой команды в текущей ветке появится новый коммит. Этот коммит будет иметь два предка – последние коммиты обоих веток, участвующих в слиянии. Содержимое этого коммита будет включать содержимое коммитов обоих веток.

## Управление ветками
Отображение списка веток в репозитории осуществляется командой *“git branch –list”* или *“git branch”*. Удаление указанной ветки осуществляется командой *“git branch -d <ветка>”*. Это «безопасная» операция, поскольку Git не позволит удалить ветку, если в ней есть неслитые изменения. Принудительное удаление указанной ветки, даже если в ней есть неслитые изменения осуществляется 
командой *“git branch -D <ветка>”*. Изменение имени текущей ветки проводится командой *“git branch -m <ветка>”*. Вывод списка всех удаленных веток – команда  *“git branch -a”*.

## Общие команды для конфликтов решения
Команда *“git status”* часто используется во время работы с Git и помогает идентифицировать конфликтующие во время слияния файлы.

### Инструменты на этапе начала слияния 
Команда *“git checkout”* может использоваться для отмены изменений в файлах или для изменения веток.
Команда *“git reset –mixed”* может использоваться для отмены изменений в рабочем каталоге или в разделе проиндексированных файлов.

### Инструменты на этапе слияния 
При выполнении команды *“git merge –abort”* процесс слияния будет прерван, а ветка вернется к состоянию, в котором она находилась до начала слияния.
Команду *“git reset”* можно использовать для разрешения конфликтов, возникающих во время выполнения слияния, чтобы восстановить заведомо удовлетворительное состояние конфликтующих файлов.

# Инструкция по работе с Git

## Что такое git?
Git  - это одна из реализаций распределенных систем контроля версий, что позволяют иметь версионность как в локальном репозитории(общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда "git init". В терминале в папке с будущим репозиторием достаточно написать "git init", и эта папка станет репозиторием.

## Создание "commits"

### Сохранение Commit
Для сохранения Commit используется комманда *"git commit"*. Для этого в терминале с папкой репозитория необходимо написать команду *git commit -m "<сообщение к коммиту>*. Сообщение к коммиту писать *** ОБЯЗАТЕЛЬНО***.

## Перемещение между "commits"
Для перемещения между коммитами необходимо использовать команду *" git checkout. Для этого в терминале с папкой репозитория  необходимо написать *"git checkout <номер коммита>*. Номер коммита берется из истории изменений. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обратное состояние используется команда *<git checkout master>*.
