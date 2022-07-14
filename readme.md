# Инструкция по работе с Git

## Что такое git?
Git  - это одна из реализаций распределенных систем контроля версий, что позволяют иметь версионность как в локальном репозитории(общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда "git init". В терминале в папке с будущим репозиторием достаточно написать "git init", и эта папка станет репозиторием.

## Создание "commits"

###  Добавление файла в "commit"
Для добавления файла в текущий коммит используется команда "git add". Для этого достаточно в терминале с папкой текущего репозитория написать "git add" *<название файла>*.

###  Добавление файла в "commit"
Для добавления файла в текущий коммит используется команда "git add". Для этого достаточно в терминале с папкой текущего репозитория написать "git add" *<название файла>*.

### Сохранение коммита
Для сохранения коммита используется комманда *"git commit"*. Для этого в терминале с папкой репозитория необходимо написать команду *git commit -m "<сообщение к коммиту>*. Сообщение к коммиту писать *** ОБЯЗАТЕЛЬНО***.

## Журнал изменений
Для просмотра историй коммитов, используется комманда *<git log>*. Для этого необходимо в терминале с папкой-репозиторием написать *git log*.

## Перемещение между "commits"
Для перемещения между коммитами необходимо использовать команду *" git checkout. Для этого в терминале с папкой репозитория  необходимо написать *"git checkout <номер коммита>*. Номер коммита берется из истории изменений. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обратное состояние используется команда *<git checkout master>*.

## Создание веток 

## Слияние веток 

## Управление ветками

## Конфликты GIT

## Команды для решения конфликтов

### Общие инструменты 

### Инструменты для начала слияния 

### Инструменты при слиянии слияния 
