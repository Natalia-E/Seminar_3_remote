# Инструкция по работе с Git и GitHub 

## Что такое git?
Git  - это одна из реализаций распределенных систем контроля версий, что позволяют иметь версионность как в локальном репозитории(общем для всех). Git является на данный момент самой популярной системой контроля версий.

## Подготовка репозитория
Для создания репозитория используется команда "git init". В терминале в папке с будущим репозиторием достаточно написать "git init", и эта папка станет репозиторием.

## Состояние репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого в терминале необходимо написать *git status* и возможно увидеть несколько состояний

1.*nothing to commit* - репозиторий не содержит изменений
2.*unversioned file* - файлу не добавлена версионность
и др.

## Создание "сохранений"

###  Добавление файла в "commit"
Для добавления файла в текущий коммит используется команда "git add". Для этого достаточно в терминале с папкой текущего репозитория написать "git add" *<название файла>*.

## Просмотр коммитов
Чтобы просмотреть разницу между текущей версией файла и версией файла в последнем коммите, используется комманда *git diff*.

### Сохранение коммита
Для сохранения коммита используется комманда *"git commit"*. Для этого в терминале с папкой репозитория необходимо написать команду *git commit -m "<сообщение к коммиту>*. Сообщение к коммиту писать *** ОБЯЗАТЕЛЬНО***.

## Журнал изменений
Для просмотра историй коммитов, используется комманда *<git log>*. Для этого необходимо в терминале с папкой-репозиторием написать *git log*.

## Перемещение между "сохранениями"
Для перемещения между коммитами необходимо использовать команду *" git checkout. Для этого в терминале с папкой репозитория  необходимо написать *"git checkout <номер коммита>*. Номер коммита берется из истории изменений. После такого "перемещения" мы попадаем в состояние *Detached head*. Для возвращения в обратное состояние используется команда *<git checkout master>*.

## Создание веток 
Ветки в GIT – представляют собой указатель на снимок изменений, - коммит. 
Если нужно добавить новую возможность или исправить ошибку (незначительную или серьезную), создается  новая ветка, в которой будут размещаться эти изменения.
Для того, чтобы создать ветку необходимо воспользоваться командой *“git branch”*  имя ветки.

## Слияние веток 
Процедура объединения веток называется слияние (merge). Для слияния текущей ветки с какой-либо другой используется команда “git merge” имя_ветки. В результате выполнения этой команды в текущей ветке появится новый коммит. Этот коммит будет иметь два предка – последние коммиты обоих веток, участвующих в слиянии. Содержимое этого коммита будет включать содержимое коммитов обоих веток.

## Управление ветками
Отображение списка веток в репозитории осуществляется командой *“git branch –list”* или *“git branch”*. Удаление указанной ветки осуществляется командой *“git branch -d <ветка>”*. Это «безопасная» операция, поскольку Git не позволит удалить ветку, если в ней есть неслитые изменения. Принудительное удаление указанной ветки, даже если в ней есть неслитые изменения осуществляется 
командой *“git branch -D <ветка>”*. Изменение имени текущей ветки проводится командой *“git branch -m <ветка>”*. Вывод списка всех удаленных веток – команда  *“git branch -a”*.

## Конфликты GIT
Конфликт во время слияния может произойти в двух отдельных точках — при запуске и во время процесса слияния. Строка ======= является «центром» конфликта. Все содержимое между этим центром и строкой <<<<<<< HEAD находится в текущей ветке main, на которую ссылается указатель HEAD. А все содержимое между центром и строкой >>>>>>> new_branch_to_merge_later является содержимым ветки для слияния.

## Команды для решения конфликтов
Команда *“git status”* часто используется во время работы с Git и помогает идентифицировать конфликтующие во время слияния файлы.
При передаче аргумента –merge для команды *“git log”* будет создан журнал со списком конфликтов коммитов между ветками, для которых выполняется слияние.
Команда *“git diff”* помогает найти различия между состояниями репозитория/файлов. Она полезна для выявления и предупреждения конфликтов слияния.

### Инструменты на этапе начала слияния 
Команда *“git checkout”* может использоваться для отмены изменений в файлах или для изменения веток.
Команда *“git reset –mixed”* может использоваться для отмены изменений в рабочем каталоге или в разделе проиндексированных файлов.

### Инструменты на этапе слияния 
При выполнении команды *“git merge –abort”* процесс слияния будет прерван, а ветка вернется к состоянию, в котором она находилась до начала слияния.
Команду *“git reset”* можно использовать для разрешения конфликтов, возникающих во время выполнения слияния, чтобы восстановить заведомо удовлетворительное состояние конфликтующих файлов.

## Получение удаленного репозитория
Для того, чтобы скачать удаленный репозиторий необходимо использовать команду *git clone*. В терминале, котором открыта любая пустая папка, необходимо написать *git clone <ссылка на репозиторий>*.Репозиторий скачается в папку, имя которой будет совпадать с именем репозитория.

## Скачивание изменений с удаленного репозитория
Для того, чтобы скачать изменения с удаленного репозитория необходимо использовать команду *git pull*.В терминале в папке с репозиторием, связанной  удаленным с репозиторием, пишем *git pull origin <название ветки>*, для того чтобы принять изменения из указанной ветки отдаленного репозитория в текущую ветку.

## Отправка изменений в GitHub
Для отправки изменений в удаленный репозиторий необходимо использовать команду *git push*. Для этого в терминале с папкой, связанной с удаленным репозиторием, пишем команду *git push origin <название ветки>*, где <название ветки> - это ветка в удаленном репозитории, куда необходимо отправить совершенные изменения.
