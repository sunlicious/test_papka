# Инструкция по работе с Гитом, а также первое домашнее задание по теме Знакомство с контролем версий, 12.05.2022

## Создание репозитория

Для создания *репозитория*, то есть папки, в которой будет вестись работа гита, нужно ввести в терминале команду 

    git init

## Создание коммитов

Commit - это фиксация изменения. Для создания *коммита*, нужно показать гиту, что отслеживать (добавить файл к отслежинваю версионности),  потом зафикисровать и для удобства присвоить комиту имя.

Чтобы показать, что отслеживать, нужно ввести в терминале команду 

    git add

### Добавление версионности

После того, как мы показали гиту, какой файл отслеживать, мы проводим редактирование нужной информации и по мере необходимости создаем сам коммит (фиксируем изменение и называем его для удобства).

Для непосредственного создания коммита вводим в терминале команду

    git commit -m "Название_коммита"

### Просмотр состояния

Статус Гита - это просмотр информации о том, на какой ветке мы находимся, есть ли измененная, не зафиксированная информация

Для того, чтобы узнать *статус*, вводим в терминале команду:

    git status

Важным замечанием является то, что при работе с Visual Studio Code каждое сохранение, прежде чем он станет доступно для Гита, должно быть сохранено сочетанием клавиш (для OS Windows): 

    Ctrl+S 

Для наглядности: 
* в случае, если выполнено сочетание клавиш Ctrl+S, статус Гита не отобразит никаких изменений;
* если Ctrl+S выполнено, но Гиту не указано, что он должен отслеживать, статус покажет нам, что есть изменения в неотслеживаемом файле (запись будет красная)
* если мы добавили файл к отсеживаемому. но пока не создали сам коммит - Гит покажет, какой файл изменился и что следует создать к нему коммит
* ну и про создании коммита - статус Гита покажет, что нет не зафиксированной информации, все наконец то сохрарено и мир в безопасности

### Просмотр списка (журнала) версий

Журнал версий - это журнал наших коммитов, с названиями. датами и временем создания, фио автора, уникальным хэш номером.

Чтобы показать *журнал версий*, нужно ввести в терминале команду

    git log

Чтобы показать *журнал всех версий всех веток*, нужно ввести в терминале команду:

    git log --all

Чтобы показать *журнал версий в сокращенном виде*, нужно  ввести в терминале команду:

    git log --oneline 

### Просмотр изменений 

Чтобы сравнить, чем отличаются коммиты, их можно сравнить. 

Для того, чтобы *сравнить коммиты*, вводим в терминале команду:

    git diff <хэш> <хэш>

При этом в терминале зеленым будет показано добавленное в этой версии, красным - удаленное.

### Переключение между коммитами

Между коммитами можно переключаться , при этом в рабочей зоне будет отображаться именно то содержанние, которое было зафиксированно в конкретном коммите. 

Чтобы *переключиться на коммит*, вводим в терминале команду:

    git checkout <хэш>

Важно помнить, что пока текущие изменения не будут зафиксированны, Гит не переключит рабочую зону на содержание того коммита, в который мы перешли. 

При переходе в другой коммит, в журнале он будет отмечен как Head, а коммит с последним актуальным содержанием - Master. 

## Создание ветки 

Для создания новой ветки используется команда:

    git branch <имя ветки>

## Удаление веток

Для удаления ветки используется команда 

    git branch -d branches

## Удаленные репозитории 

Получение данных об удаленных репозиториях
