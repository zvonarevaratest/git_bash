# Работа с git и bash

**Задача 1:**

1. Предварительно создайте файл bash1.txt, в который вы будете добавлять выполненные команды. 
\
``touch bash1.txt``
1. Открыть домашнюю директорию через терминал 
\
`cd`
1. Определить имя папки, в которой вы находитесь 
\
`pwd`

1. Создать внутри этой папки каталог с именем test1 
\
`mkdir test1`

1. Перейти в папку test1  
\
`cd test1`

1. Создать файл 1,2 и 3 внутри каталога test1 
\
`touch 1 2 3`

1. Проверить содержимое каталога test1 
\
`ls`

1. Перейти в домашнюю директорию 
\
`cd`

1. Создать папку test2 внутри домашней директории 
\
`mkdir test2`

1. Удалить папку test2 
\
`rmdir test2`

1. Удалить файл 2 из папки test1  
\
`rm ~/test1/2`

1. Создать папку в домашней директории test3 и добавить в нее два файла 
\
`mkdir test3 && touch test3/1.txt test3/2.txt`

1. Удалить папку test3 
\
`rm -r test3`

1. Создать папку test4 в домашней директории  
\
`mkdir test4`

1. Переместить файлы 1 и 3 из папки test1 в папку test4 
\
mv test1/* test4

1. Добавить в файл 1 три строки со словами line 
\
`echo line > test4/1.txt && echo line >> test4/1.txt && echo line >> test4/1.txt`

1. Посмотреть содержимое файла 1 
\
`cat test4/1.txt`

1. Добавьте в файл 3 три строки со словами line 
\
`echo line > test4/3.txt && echo line >> test4/3.txt && echo line >> test4/3.txt`

1. Просмотрите содержимое двух файлов (1 и 3) сразу 
\
`cat test4/1.txt test4/3.txt`

1. Используя один из редакторов замените все строки в файле 1 
\
`nano test4/1.txt`

**Задача 2**

1. Предварительно создайте файл bash2.txt, в который вы будете добавлять выполненные команды. 
\
`touch bash2.txt`

2. Зайти в домашнюю директорию через терминал. 
\
`cd`

3. Создать папку test 3.  
\
` mkdir test3`
4. Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
```
echo row1 > test3/4.txt
echo row2 >> test3/4.txt
echo row3 >> test3/4.txt
echo row4 >> test3/4.txt
cp test3/4.txt test3/5.txt
cp test3/4.txt test3/6.txt
```

5. Найдите строку row2 в файле 5
\
`grep row2 test3/5.txt`

6. Найдите строку row2 в файле 5
\
`grep -r "row" test3`

7. Посчитайте сколько строк с содержимым row в файле 6
\
`grep row test3/6.txt | wc -l`

8. Найдите файл 5 внутри папки test3
\
`find test3 -name "5.txt”`

9. Используя команду find, удалите файл 5
\
`find test3 -name "5.txt" -exec rm {} \; ) (find test3 -name "5.txt" | xargs rm`

10. Используя команду echo, добавьте слово test в файл 4
\
`echo "test"> test3/4.txt`

11. Замените слово test в файле 4 на fail
\
`nano test3/4.txt`

12. Добавьте в файл 4 слово test так, чтобы сохранилось содержимое
\
`echo "test">> test3/4.txt`

13. Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе
\
`ps aux`

14. Убейте процесс 666 в консоли
   \
`kill 666`

15. Узнайте доступность ресурса artsiomrusau.com, используя ping
\
`ping artsiomrusau.com`

16. Отправьте 5 пакетов на сайт artsiomrusau.com
\
`ping -c 5 artsiomrusau.com`

17. Используя GET и команду curl, получите информацию о зарегистрированных питомцах на `https://petstore.swagger.io/`
```bash
curl -X 'GET' \
  'https://petstore.swagger.io/v2/pet/findByStatus?status=available' \
  -H 'accept: application/json'
```

18. Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/
```jsx
curl -X 'POST' \
'https://petstore.swagger.io/v2/user' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-d '{
"username": "zrimma",
"firstName": "Rimma",
"lastName": "Zvonareva",
"email": "[zvonarevara@gmail.com](mailto:zvonarevara@gmail.com)",
"password": "qwerty123",
"phone": "+799999999"
}'
```
