# Terminal_GitBash
1) Посмотреть где я
+ `pwd`

2) Создать папку
+ `mkdir` foldername

3) Зайти в папку
+ `cd` foldername

4) Создать 3 папки
+ `mkdir` foldername1 foldername2 foldername3
+ `mkdir` foldername{1,2,3}
+ `mkdir` foldername{1..3}

5) Зайти в любоую папку
+ `cd` foldername1

6) Создать 5 файлов (3 txt, 2 json)
+ `touch` file1.txt file2.txt file3.txt file4.json file5.json
+ `touch` file{1,2,3}.txt file{4,5}.json

7) Создать 3 папки
+ `mkdir` foldername_{1..3}

8) Вывести список содержимого папки
+ `ls` 			- показывает содержимое текущей папки
+ `ls -f`		- показывает содержимое текущей папки, включая скрытые файлы
+ `ls -l`		- показывает содержимое текущей папки структурировано, кроме скрытых
+ `ls -a`		- показывает содержимое текущей папки
+ `ls -l -a`		- показывает содержимое текущей папки разширено (разрешения, владелец, размер, дата изменения)
+ `ls -la`		- тоже самое, но сокращенно
+ `ls ..` 		- показывает содержимое папки выше без выхода из текущей
+ `ls -lt`		- показывает содержимое текущей папки с сортировкой по дате создания файлов
+ `ls -lu`		- показывает содержимое текущей папки с сортировкой по дате обращения к файлам
+ `ls -lt`	 	- показывает содержимое текущей папки с сортировкой по дате создания файлов
+ `ls -lu` 		- показывает содержимое текущей папки с сортировкой по дате обращения к файлам
+ `ls /c/foldername/foldername1` - показывает содержимое папки foldername1 по пути не выходя из текущей

9) Открыть любой txt файл
+ `vim` file1.txt

10) Написать в созданный файл любой текст.
+ нажать `"i"` для возможности ввода(редактирования) данных

+ написать "Lorem ipsum dolor sit amet, consectetur adipiscing elit,
	sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
	Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
	reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
	pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
	culpa qui officia deserunt mollit anim id est laborum"

11) Сохранить внесенные данные и выйти
+ нажать `"esc"` ввести `:wq`

12) Выйти из папки на уровень выше
+ `cd ..`

13) Переместить любые 2 файла, которые вы создали, в любую другую папку.
+ `mv` foldername1/{file1.txt,file4.json} foldername1/foldername_3

14) Скопировать любые 2 файла, которые вы создали, в любую другую папку.
+ `cp` foldername1/{file2.txt,file5.json} foldername1/foldername_2

15) Найти файл по имени
+ `find . -name` "file1.txt" 		- если мы знаем формат файла
+ `find . -name` "file1.*"		- если не знаем формат файла

16) Просмотреть содержимое в реальном времени
+ `tail -f` file1.txt - вывод содержимого и его последующих изменений в консоль
+ `tail -f` file1.txt | `grep --line-buffered` laborum >> file_log.txt - запись изменений в тектовый файл после "laborum"

17) Вывести 3 первые строки из текстового файла
+ `head -3` file1.txt

18) Вывести 3 последние строк из текстового файла
+ `tail -3` file1.txt

19) Просмотреть содержимое длинного файла.
+ `less` file1.txt
+ нажать `q` для выхода из режима просмотра

20) Вывести дату и время
+ `date`

Задание *
```
1) Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request
	1) curl "http://162.55.220.72:5005/terminal-hw-request"
	- Ответ {"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1"
:"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_
your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}
	2)  curl "http://162.55.220.72:5005/get_method?name=(Alona)&age=(25)"
	- Ответ ["(Alona)","(25)"]
```
```
2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
    1. touch script - создать файл скрипт
    2. vim script	- открыть файл скрипт для редактирования
    3. нажать "i"
    4. ввести название используемой оболочки - #!/bin/bash
    5. ввести данные:
	* cd foldername
	* mkdir foldername{1..3}
	* cd foldername1
	* touch file{1,2,3}.txt file{4,5}.json
	* mkdir foldername{1..3}
	* ls
	* mv {file1.txt,file4.json} foldername_3
    6. нажать "esc" ввести :wq - сохранить и выйти
    7. Сделать файл исполняемым - chmod +x ./script
    8. Запустить скрипт ./script
```


