# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
---
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория
---
Для создание репозитория необходимо выполнить команду git init в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Ввод информации
---
Когда репозиторий готов, Вы можете ввести всю нужную вам информацию в **рабочую область**.

## Сохранение файла и запись изменений
---
После того, как Вы внесли ввели нужную Вам информацию, можно **сохранить файл** и тем самым записать его **новую версию**.

Для этого мы делаем несколько шагов:

1. Сохраняем файл любым удобным способом: *Файл* => *Сохранить* , либо *Ctrl + S* , либо включить Автосохранение, чтобы не заниматься рутинным занятием и не забыть в неподходящий момент пропустить важную точку сохранения. Включается так: *Файл => Автосохранение*. **Без сохранения файла мы не сможем записать новую версию.**
2. Вводим в терминал команду *git add .\название файла* с его расширением, например: *git add .\First_file.md* . **Таким образом мы добавляем к нашему файлу внесённые изменения для последующей записи.**
3. После процедуры *git add* мы должны произвести запись внесённых изменений создав **новую версию**. Введём команду *git commit -m "Любой текст"* . В данной команде *commit* является функцией записи новых изменений, а флаг *-m* означает, что после него в кавычках будет написан комментарий к этим изменениям. **После ввода данной команды все изменения записаны в новую версию.**

## Проверка иземнений
---
В случае, когда нужно узнать какие изменения были внесены в файл и все эти изменения были сделаны после функции *commit* , можно воспользоваться командой *git status* и *git diff*: ***git status* покажет какие этапы ещё не завершены и может помочь в случае, если непонятно был сделан *commit* к примеру или нет.** **В свою очередь *git diff* покажет процесс изменений файла после записи commit и до момента, когда мы его записали.**

## Просмотр списка версий и переход к версии
---
Когда у нас существует потребность в переходе к более старой и стабильной версии мы используем ряд команд:

* **git log** - покажет список версий с отображением сверху вниз от новой к старой.
* **git checkout** - данная команда даёт возможность перейти к любой из версий, главным условием является указание версии. Например старая версия **12qw34er** , а новая версия **34er12qw**. Находясь в новой версии комманда будет выглядеть так: ***git checkout 12qw3*** отмечу, что обычно достаточно ввести первые 4 символа версии. Также, при большом количестве версий, мы можем использовать имя ***main*** или ***master***(зависит от варианта программы) для быстрого перехода к актуальной версии. Выглядит так ***git checkout main***

* Также добавлю, что для более комфортного просмотра списка версий существует комманда ***git log --oneline*** когда список версий будет показан в виде одиночных строк с первыми 7ю символами и комментарием к записи.

## Применение знаков для работы с текстом
---
В **git** можно использовать разные знаки для форматирования текста:

* **Звёздочка с пробелом** перед текстом создаст ненумерованный список * текст
* **Цифра с точкой и пробелом** создаст нумерованный список 1. текст
* **Знак решётки** определяет заголовок c подчёркиванием # текст
* **Две решётки** более маленький заголовок без подчёркивание ## текст
* **Звёздочка без пробелов** до и после информациiи преобразует стиль текста в курсив * текст *
* **Две звёздочки без пробелов** до и после информации преобразуют стиль текста в полужирный ** текст **
* Используя **три звёздочки** можно получить микс курсива и полужирного *** текст ***
* **4 значка тильды**(2 до и 2 после информации) делают текст зачёркнутым ~~ текст ~~
* С помощью **трёх знаков тире(минус)** можно выполнять подчёркивание как у заголовка ---

## ~~Здесь был Russian Lord~~

## Создания и слияние веток
---
В git мы можем создавать ветки, это удобно для параллельной разработки файла.
Чтобы создать ветку нужно написать в терминале ***git branch branch_name*** (где branch_name это любое удобное имя для ветки)

После того, как ветка создана, мы можем работать в ней независимо от основной или других веток. При этом дополнительно при команде ***git log --graph*** покажет помимо текущей ветки также и основную, но не покажет другие ветки, т.к. они полностью независимы.

Чтобы объединить ветки в одну(слить), нужно выполнить команду ***git merge branch_name*** при этом важно то, где мы находимся. Мы можем быть в основной ветке ***main***, а можем быть в любой другой. Поэтому если мы находимся в ветке, к примеру, ***main***, то введя команду мы сольём эту ветку с другой, все изменения запишутся в ветку где мы находимся.

## Удаление веток
---
Для удаления ветки мы выполняем команду ***git branch -d branch_name*** , флажок ***-d*** отвечает за удаление.

## Добавление изображений и .gitignore
---
Для того, чтобы добавить изображение, мы должны перенести файл изображения в рабочу папку и в рабочем окне вписать
***![имя для картинки!](название файла с его расширением)***
А, чтобы этот файл картинки не спамил ошибкой, нужно создать файл ***.gitignore*** и вписать название файла с его расширением в рабочее окно.

## VR убивает!!!
=========================================================================================================
![vr опасен!](9f8.jpg)

Тест сихнронизации баз
Сонхронка с удалёнки
