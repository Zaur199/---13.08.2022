# Инструкция по работе с Git

## Что такое Git
*Git* - одна из реализаций распределённых систем контроля версий, позволяющая организовать версионность, как локально, так и на удалённом сервере. Самая популярная платформа, реализующая *Git*, - [GitHub](https://github.com)

## Подготовка репозитория
Для создания в папке репозитория необходимо открыть эту папку в терминале и написать команду "git init", после чего в этой папке создасться скрытая папка "git", и таким образом папка станет репозиторием

### Просмотр состояния репозитория
Для просмотра состояния репозитория используется команда *git status*. В терминале с открытой папкой-репозиторием необходимо написать команду *git status*. В результате можно увидеть следующие выводы:
1. On branch *** nothing to commit - это означает нет активных изменений
2. Untracked files - это означает, что имеются файлы, не отслеживаемые системой контроля версий
...

### Добавление файла к "сохранению"
Для того, чтобы добавить файл к "сохранению" необходимо использовать команду *git add*. В терминале с открытой папкой-репозиторием необходимо написать *git add <название файла>*, и этот файл добавиться к "сохранению"

## Создание фиксации
Для создания фиксации используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m <сообщение к комиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**.

## Журнал изменений
Для просмотра истории изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*, и Вы увидите список всех коммитов в этой ветке с описанием: имени, электронной почты, сообщение к коммиту и номер коммита.

## Перемещение между коммитами
Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <номер коммита>*. Номер коммита берётся изжурнала изменений ветки.

## Ветвление в git

## Слияние веток и слияние конфликтов
Слияние веток – это перенос изменений с одной ветки на другую. При этом слияние не затрагивает сливаемую ветку, то есть она остается в том же состоянии, что позволяет нам потом продолжить работу с ней.
Чтобы выполнить мердж (от англ. merge – слияние), в Git предусмотрена команда git merge. Формат:
git merge <сливаемая ветка>.
Итак, git merge делает следующие шаги:
1. Проверяет, нет ли конфликтов, т.е. не удалят и не перепишут ли наши изменения какую-либо уже существующую информацию. Если возникает конфликт git merge останавливается, чтобы получить инструкции от пользователя;
2. Добавляет все изменения из коммитов в индекс ветки master;
3. Делает коммит

Если Git обнаруживает, что изменения, внесенные в одну ветвь, конфликтуют с изменением, сделанным в другой, он предложит устранить конфликт. Конфликт слияния может возникать, когда объединенные ветви изменяют одну и ту же строку файла по-разному или когда одна ветвь изменяет файл, а другая ветвь удаляет ее.
 Можно разрешить конфликты слияния в Visual Studio или с помощью командной строки и любого текстового редактора.

## Удаление веток
<<<<<<< HEAD

## Заключение
Рассмотрев принцип работы *GIT*, можно сделать следующие выводы:
1. Защищает исходный код от потери. ...
2. Обеспечивает командную работу. ...
3. Помогает отменить изменения. ...
4. Распределённая работа.
=======
Чтобы удалить локальную ветку GIT, вы можете выполнить одну из следующих команд:
+ git branch -d branch_name
+ git branch -D branch_name

Как вы можете заметить, эти команды, в разных вариациях использования, имеют 2 разных аргумента, d и D.
Параметр -d означает --delete, который удалит локальную ветвь, только в случае, если вы смерджили её с какой-то из веток.
Опция -D обозначает --delete --force, которая удаляет ветку независимо от ее статуса push или merge, так что будьте осторожны при её использовании!
>>>>>>> gitDelete
