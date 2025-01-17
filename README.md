# D01_Linux stephenk

## **== Задание 1 ==**

### Установи **Ubuntu 20.04 Server LTS** без графического интерфейса. (Используем программу для виртуализации - VirtualBox)

- Графический интерфейс должен отсутствовать.
- Узнай версию Ubuntu, выполнив команду
    
    `cat /etc/issue`
    
- Вставь скриншот с выводом команды.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/4c3e54fc-2fb7-419d-bcb3-de2dbe852b7a.png)

Скриншот 1 - Вывод cat /etc/issue

## **== Задание 2==**

### Создай пользователя, отличного от созданного при установке. Пользователь должен быть добавлен в группу `adm`.

- Вставь скриншот вызова команды для создания пользователя.
- Новый пользователь должен быть в выводе команды `cat /etc/passwd`
- Вставь скриншот с выводом команды.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/ede124bf-8049-4097-b929-b09cd9402dc2.png)

Скриншот 2 - testuser в /etc/passwd

sudo useradd -G adm -p qwerty -m -s /bin/bash testuser

## **== Задание 3==**

### Задай название машины вида user-1.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/9b4afa4c-2ae7-49f8-befa-40369f85221b.png)

Скриншот 3 - Новое имя машины

### Установи временную зону, соответствующую твоему текущему местоположению.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/d1042c9a-6cd6-4035-ade2-27335438a507.png)

Скриншот 4 - Установка часового пояса 

### Выведи названия сетевых интерфейсов с помощью консольной команды.

- В отчёте дай объяснение наличию интерфейса lo.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/9778d1d4-d4f9-4909-9ff2-66ac440404ce.png)

Скриншот 5 - Интерфейсы

*lo* (loopback device) – виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес *127.0.0.1*. У него есть dns-имя – *localhost*. Посмотреть привязку можно в файле */etc/hosts*.

### Используя консольную команду, получи ip адрес устройства, на котором ты работаешь, от DHCP сервера.

- В отчёте дай расшифровку DHCP.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/3f4c4c3d-e761-48a8-aa23-97f077885431.png)

Скриншот 6 - ip интерфейсов

**DHCP** (англ. *Dynamic Host Configuration Protocol* — протокол динамической настройки узла) — сетевой протокол, позволяющий сетевым устройствам автоматически получать IP-адрес и другие параметры, необходимые для работы в сети TCP/IP.

### Определи и выведи на экран внешний ip-адрес шлюза (ip) и внутренний IP-адрес шлюза, он же ip-адрес по умолчанию (gw).

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/f08f21e5-f6c9-428b-a0f0-e524299a667b.png)

Скриншот 7 -  Внешний ip

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/773a6523-df47-4389-b5d9-a2c99754f818.png)

Скриншот 8 - Внутренний ip

### Задай статичные (заданные вручную, а не полученные от DHCP сервера) настройки ip, gw, dns (используй публичный DNS серверы, например 1.1.1.1 или 8.8.8.8).

 

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/68c56582-d1de-44bc-a02f-843ab1cad7b8.png)

Скриншот 9 - Настройки статичного ip

### Перезагрузи виртуальную машину. Убедись, что статичные сетевые настройки (ip, gw, dns) соответствуют заданным в предыдущем пункте.

- В отчёте опиши, что сделал для выполнения всех семи пунктов (можно как текстом, так и скриншотами).
- Успешно пропингуй удаленные хосты 1.1.1.1 и ya.ru и вставь в отчёт скрин с выводом команды. В выводе команды должна быть фраза «0% packet loss».

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/be904d43-c8b3-49ba-a4bf-c136c398ebfe.png)

Скриншот 10 - пинг указаных адресов

## **== Задание 4==**

### Обнови системные пакеты до последней на момент выполнения задания версии.

- После обновления системных пакетов, если ввести команду обновления повторно, должно появиться сообщение, что обновления отсутствуют;
- Вставь скриншот с этим сообщением в отчёт.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/039b79a0-f361-491a-9050-6ee39de56672.png)

Скриншот 11 - обновление системы 1

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled.png)

Скриншот 12 - обновление системы 2

sudo apt update

sudo apt upgrade

## **== Задание 5==**

### Разреши пользователю, созданному в [Part 2](https://www.notion.so/D01_Linux-stephenk-ca153033db6f40efac2f2a2cc00f1d17?pvs=21),выполнять команду sudo.

- В отчёте объясни *истинное* назначение команды sudo (про то, что это слово - «волшебное», писать не стоит);

sudo позволяет запускать команды от имени других пользователей, по умолчанию от имени суперпользователя.

- Поменяй hostname ОС от имени пользователя, созданного в пункте [Part 2](https://www.notion.so/D01_Linux-stephenk-ca153033db6f40efac2f2a2cc00f1d17?pvs=21) (используя sudo);
- Вставь скрин с изменённым hostname в отчёт.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/5762f5ee-3c34-4186-aa15-228d4bf9b2ae.png)

Скриншот 13 - переименовние машины от testuser

## **== Задание 6==**

### Настрой службу автоматической синхронизации времени.

- Выведи время часового пояса, в котором ты сейчас находишься.
- Вывод следующей команды должен содержать `NTPSynchronized=yes`: `timedatectl show`
- Вставь скрины с корректным временем и выводом команды в отчёт.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/7158fd10-20fd-48e6-8263-424850b8b70c.png)

Скриншот 14 - установка NTP

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/841fbd44-df34-4c75-8d76-3ac3f21332eb.png)

Скриншот 15 - проверка синхронизации времени

## **== Задание 7==**

### Установи текстовые редакторы **VIM** (+ любые два по желанию **NANO**, **MCEDIT**, **JOE** и т.д.)

### Используя каждый из трех выбранных редакторов, создай файл *test_X.txt*, где X -- название редактора, в котором создан файл. Напиши в нём свой никнейм, закрой файл с сохранением изменений.

- В отчёт вставь скриншоты:
    - Из каждого редактора с содержимым файла перед закрытием;
- В отчёте укажи, что сделал для выхода с сохранением изменений.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%201.png)

Скриншот 16 - Изменение файлов в nano

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%202.png)

Скриншот 17 - Изменение файлов в Vim

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%203.png)

Скриншот 18 - изменение файлов в mcedit

nano: Ctrl + X и да на вопрос о сохранении

Vim: :wq

mcedit: f10 и да на вопрос о сохранении

### Используя каждый из трех выбранных редакторов, открой файл на редактирование, отредактируй файл, заменив никнейм на строку «21 School 21», закрой файл без сохранения изменений.

- В отчёт вставь скриншоты:
    - Из каждого редактора с содержимым файла после редактирования;
- В отчёте укажи, что сделал для выхода без сохранения изменений.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%204.png)

Скриншот 19 - Выход без сохранения nano

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%205.png)

Скриншот 20 - Выход без сохранения Vim

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%206.png)

Скриншот 21 - Выход без сохранения mcedit

### Используя каждый из трех выбранных редакторов, отредактируй файл ещё раз (по аналогии с предыдущим пунктом), а затем освой функции поиска по содержимому файла (слово) и замены слова на любое другое.

- В отчёт вставь скриншоты:
    - Из каждого редактора с результатами поиска слова;
    - Из каждого редактора с командами, введёнными для замены слова на другое.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%207.png)

Скриншот 22 - Поиск по файлу nano

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%208.png)

Скриншот 22 - замена nano

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%209.png)

Скриншот 23 - Команда для поиска и замены Vim

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2010.png)

Скриншот 24 - Поиск по файлу Vim

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2011.png)

Скриншот 25 -  Замена Vim

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2012.png)

Скриншот 26 - Окно поиска по файлу mcedit

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2013.png)

Скриншот 27 - Поиск по файлу mcedit

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2014.png)

Скриншот 28 - Замена mcedit

## **== Задание 8==**

### Установи службу SSHd.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2015.png)

Скриншот 29 - Установка SSHd

### Добавь автостарт службы при загрузке системы.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/540310c2-67f8-49b6-b0cc-0f21052f661a.png)

Скриншот 30 - автостарт при запуске системы

### Перенастрой службу SSHd на порт 2022.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2016.png)

Скриншот 31 - конфигурационный файл SSHd

### Используя команду ps, покажи наличие процесса sshd. Для этого к команде нужно подобрать ключи.

- В отчёте объясни значение команды и каждого ключа в ней.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2017.png)

Скриншот 32 - процесс SSHd

ps выводит процессы, запущенные в системе. Ключ -A выводит все процессы, в том числе фоновые, системные, других пользователей. 

### Перезагрузи систему.

- В отчёте опиши, что сделал для выполнения всех пяти пунктов (можно как текстом, так и скриншотами).
- Вывод команды netstat -tan должен содержать `tcp 0 0 0.0.0.0:2022 0.0.0.0:* LISTEN` 
(если команды netstat нет, то ее нужно установить)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2018.png)

Скриншот 33 - Скрин с выводом команды

- Скрин с выводом команды вставь в отчёт.
- В отчёте объясни значение ключей -tan, значение каждого столбца вывода, значение 0.0.0.0.

t - показать tcp порты

a - показать все порты

n - показать ip в числовом виде

- `Proto` — протокол (tcp, udp, raw), используемый сокетом.
- `Recv-Q` — количество байтов, не скопированных локальным приложением.
- `Send-Q` — количество байтов, не подтвержденных удаленным хостом.
- `Local Address` — адрес и номер порта локального конца сокета.
- `Foreign Address` — адрес и номер порта удаленного конца сокета.

0.0.0.0 - значение адреса по умолчанию т.е. конкретного ip ещё не задали.

## **== Задание 9==**

### Установи и запусти утилиты top и htop.

- По выводу команды top определи и напиши в отчёте:
    - uptime - 30 min
    - количество авторизованных пользователей - 1
    - общую загрузку системы - 0
    - общее количество процессов - 95
    - загрузку cpu - 0.3%
    - загрузку памяти - 138,6 Мбайт
    - pid процесса занимающего больше всего памяти- 671 (Shift + m)
    - pid процесса, занимающего больше всего процессорного времени - 120 (Shift + p)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2019.png)

Скриншот 34 - top

- В отчёт вставь скрин с выводом команды htop:
    - отсортированному по PID, PERCENT_CPU, PERCENT_MEM, TIME
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2020.png)
    
    Скриншот 35 - Сортировка по PID
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2021.png)
    
    Скриншот 36 - Сортировка по PERCENT_CPU
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2022.png)
    
    Скриншот 37 - Сортировка по PERCENT_MEM
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2023.png)
    
    Скриншот 38 - Сортировка по TIME
    
    - отфильтрованному для процесса sshd
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2024.png)
    
    Скриншот 39 - С фильтром SSHd
    
    - с процессом syslog, найденным, используя поиск
    
    ![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2025.png)
    
    Скриншот 38 - Поиск syslog
    
    - с добавленным выводом hostname, clock и uptime

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2026.png)

Скриншот 39 - Добавленные поля

## **== Задание 10==**

### Запусти команду fdisk -l.

- В отчёте напиши название жесткого диска, его размер и количество секторов, а также размер swap.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2027.png)

Скриншот 40 - Вывод fdisk -l

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/fa175dd8-db6c-4a00-9e29-1b675701810d.png)

Скриншот 41 - swap файл

## **== Задание 11==**

### Запусти команду df.

- В отчёте напиши для корневого раздела (/):
    - размер раздела - 11758760
    - размер занятого пространства - 4962992
    - размер свободного пространства - 617660
    - процент использования - 45
- Определи и напиши в отчёт единицу измерения в выводе - Кбайт

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2028.png)

Скриншот 42 - вывод df

### Запусти команду df -Th.

- В отчёте напиши для корневого раздела (/):
    - размер раздела - 12G
    - размер занятого пространства - 4,8G
    - размер свободного пространства - 5,9G
    - процент использования - 45%
- Определи и напиши в отчёт тип файловой системы для раздела - ext4

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2029.png)

Скриншот 43 - вывод df -Th

## **== Задание 12==**

### Запусти команду du

### Выведи размер папок /home, /var, /var/log (в байтах, в человекочитаемом виде)

du -b - в байтах

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2030.png)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2031.png)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2032.png)

du -h - Человекочитаемый вид

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2033.png)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2034.png)

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2035.png)

Скриншоты 44-49 - du c нужными папками

### Выведи размер всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя *)

- В отчёт вставь скрины с выводом всех использованных команд.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2036.png)

Скриншот 50 - du -a /var/log/*

## **== Задание 13==**

### Установи утилиту ncdu

### Выведи размер папок /home, /var, /var/log

- Размеры должны примерно совпадать с полученными в [Part 12](https://www.notion.so/D01_Linux-stephenk-ca153033db6f40efac2f2a2cc00f1d17?pvs=21).
- В отчёт вставь скрины с выводом использованных команд.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2037.png)

Скриншот 51 - ncdu /home

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2038.png)

Скриншот 52 - ncdu /var

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2039.png)

Скриншот 53 - ncdu /var/log

## **== Задание 14==**

### Открой для просмотра:

### 1. /var/log/dmesg

### 2. /var/log/syslog

### 3. /var/log/auth.log

- Напиши в отчёте время последней успешной авторизации, имя пользователя и метод входа в систему;
- Перезапусти службу SSHd;
- Вставь в отчёт скрин с сообщением о рестарте службы (искать в логах).

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2040.png)

Скриншот 54 - /var/log/dmesg

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2041.png)

Скриншот 55 - /var/log/syslog

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2042.png)

Скриншот 56 - /var/log/auth.log c последним логином и перезапуском SSHd

## **== Задание 15==**

### Используя планировщик заданий, запусти команду uptime через каждые 2 минуты.

- Найди в системных журналах строчки (минимум две в заданном временном диапазоне) о выполнении;
- Выведи на экран список текущих заданий для CRON;
- Вставь в отчёт скрины со строчками о выполнении и списком текущих задач.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2043.png)

Скриншот 57 - CRON в журналах 

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2044.png)

Скриншот 58 - задача в crontab

### Удали все задания из планировщика заданий.

- В отчёт вставь скрин со списком текущих заданий для CRON.

![Untitled](D01_Linux%20stephenk%20ca153033db6f40efac2f2a2cc00f1d17/Untitled%2045.png)

Скриншот 59 - Удалены все задачи CRON