# LR6
Лабораторная работа №6

**Цель лабораторной работы:** изучение базовых возможностей системы
управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием.

**Ход работы:**
Для начала создал [аккаунт](https://github.com/YABEZDELNIK) на сайте GitHub.<br>
На гитхабе сделал копию в личное хранилище из https://github.com/Kurtyanik/LR6/.<br>
Установил Git и настроил клиент путем ввода имени пользователя и email с помощью команд git config --global user.name "4917 Borodinov D. A." и git config --global user.email dimon2405@list.ru<br>
Следом я клонировал удаленный репозиторий себе на компьютер с помощью команды git clone https://github.com/Kurtyanik/LR6/<br>
	![Рисунок 1](/Screenshots/1.png)<br>
	Рисунок 1 - настройка клиента и клонирование репозитория<br>
Далее я перешел в ветку branch1, добавил файл и отредактировал его с помощью интерфейса GitHub), после чего подтянул изменения в локальный репозиторий. Для этого я использовал команды cd LR6, чтобы зайти в локальный репозиторий, git checkout branch1, чтобы перейти в ветку branch1 и подтянул изменения с помощью команды pit pull https://github.com/YABEZDELNIK/LR6/ branch1<br>
	![Рисунок 2](/Screenshots/2.png)<br>
        Рисунок 2 - Создание и редактирование файла<br>
	![Рисунок 3](/Screenshots/3.png)<br>
        Рисунок 3 - Применение создания файла<br>
	![Рисунок 4](/Screenshots/4.png)<br>
        Рисунок 4 - Файл в репозитории<br>
	![Рисунок 5](/Screenshots/5.png)<br>
        Рисунок 5 - Переход в ветку branch1 и подтягивание изменений<br>
Следом получаем историю операций каждой ветки с помощью команды git log
	![Рисунок 6](/Screenshots/6.png)<br>
        Рисунок 6 - История операций ветки branch1<br>
	![Рисунок 7](/Screenshots/7.png)<br>
        Рисунок 7 - История операций ветки master<br>
Следующим шагом выполняем слияние в ветку master, разрешая конфликт. Для этого использую команды git merge branch1, находясь в ветке master, vim mergefile.txt для редактирования конфликтующего файла, git add mergefile.txt и git commit для подтверждения редактирования.<br>
	![Рисунок 8](/Screenshots/8.png)<br>
        Рисунок 8 - Выполнение команды слияния веток<br>
	![Рисунок 9](/Screenshots/9.png)<br>
        Рисунок 9 - Редактирование конфликтующего файла<br>
	![Рисунок 10](/Screenshots/10.png)<br>
        Рисунок 10 - Подтверждение изменений<br>
	![Рисунок 11](/Screenshots/11.png)<br>
        Рисунок 11 - Повторная попытка слияния<br>
Далее я удаляю ветку branch1, используя команду git branch -D branch1<br>
	![Рисунок 12](/Screenshots/12.png)<br>
        Рисунок 12 - Удаление ветки branch1<br>
Применяем изменения к удаленному репозиторию командой git push https://github.com/YABEZDELNIK/LR6/ master<br>
	![Рисунок 13](/Screenshots/13.png)<br>
        Рисунок 13 - Применение изменений к удаленному репозиторию<br>
Следом я добавил два файла и коммитнул их с помощью команд vim файл1.txt, vim файл2.txt для создания файлов, git add \* и git commit -m 'Добавил два файла' для коммита<br>
	![Рисунок 14](/Screenshots/14.png)<br>
        Рисунок 14 - Добавление первого файла<br>
	![Рисунок 15](/Screenshots/15.png)<br>
        Рисунок 15 - Добавление второго файла<br>
	![Рисунок 16](/Screenshots/16.png)<br>
        Рисунок 16 - Коммит добавления файлов<br>
После этого делаем хард откат на 1 коммит командой git reset --hard HEAD~1<br>
	![Рисунок 17](/Screenshots/17.png)<br>
        Рисунок 17 - Хард откат коммита<br>
Далее получаем расширенный лог, используя команду git log --pretty=format:"%h - %ad %an : %s"<br>
	![Рисунок 18](/Screenshots/18.png)<br>
        Рисунок 18 - Получение расширенного лога команд<br>
В папке репозитория открываем папку .git, в ней папку logs, открываем файл HEAD, и тем самым получаем полный лог<br>
	![Рисунок 19](/Screenshots/19.png)<br>
        Рисунок 19 - Получение полного лога<br>
Загружаем большую часть скриншотов в удаленный репозиторий командами git add \*, git status и git commit -m 'Добавил почти все скриншоты'<br>
	![Рисунок 20](/Screenshots/20.png)<br>
        Рисунок 20 - Загрузка скриншотов в удаленный репозиторий<br>
	![Рисунок 21](/Screenshots/21.png)<br>
        Рисунок 21 - Загрузка скриншотов в удаленный репозиторий<br>
Удаляем ненужные ветки в удаленном репозитории с помощью команды git push https://github.com/YABEZDELNIK/LR6/ --delete \*Название ветки\*<br>
	![Рисунок 22](/Screenshots/22.png)<br>
        Рисунок 22 - Удаление веток в удаленном репозитории<br>
Применяем все изменения к удаленному репозиторию (во всех ветках) с помощью команды git push https://github.com/YABEZDELNIK/LR6/ \*Название ветки\*<br>
	![Рисунок 23](/Screenshots/23.png)<br>
        Рисунок 23 - Применение всех изменений к удаленному репозиторию<br>
	![Рисунок 24](/Screenshots/24.png)<br>
        Рисунок 24 - Применение всех изменений к удаленному репозиторию<br>

**Вывод:** изучил базовые возможности системы управления версиями, получил опыт работы с Git Api, а также опыт работы с локальным и удаленным репозиторием.
