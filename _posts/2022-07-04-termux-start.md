---
layout: post
title:  "Termux-начало"
date:   2022-07-04 9:28:13 +0300
categories: linux
excerpt: 'Termux — это эмулятор терминала Android и приложение для среды Linux.'
description: Termux — это эмулятор терминала Android и приложение для среды Linux.
permalink: /termux-start/
---

## Несколько нужных команд


* ls # – отображает список файлов и директорий в текущей директории 
* cd # – перемещает в указанную директорию, например: Важно понимать: если путь не указан прямо (~/storage/downloads/1.txt) он будет от текущей директории 
   * cd dir1 # – переместит в dir1 если в текущей директории она есть cd ~/dir1 # – переместит в dir1 по указанному пути от корневой папки 
   * cd #  или cd ~ # - переместить в корневую папку 
* clear # – очищаем консоль 
* ifconfig # – можно посмотреть IP, а можно и сеть настроить 
* cat # – позволяет работать с файлами/устройствами (в рамках одного потока) например: 
* cat 1.txt # – просмотрим содержимое файла 
* 1.txt cat 1.txt>>2.txt # – копируем файл 1.txt в файл 2.txt  (файл 1.txt останется) 
* rm # - используемая для удаления файлов из файловой системы. Ключи, использующиеся с rm:
   * -r # – обрабатывать все вложенные директории. Данный ключ необходим, если удаляемый файл является директорией. Если удаляемый файл не является директорией, то ключ -r не влияет на команду rm. 
   * -i # – выводить запрос на подтверждение каждой операции удаления. 
   * -f # – не возвращать код ошибочного завершения, если ошибки были вызваны несуществующими файлами; не запрашивать подтверждения операций. Например: rm -rf mydir # – удалить без подтверждения и кода ошибочного завершения файл (или каталог) mydir. 
* mkdir <путь> # – создает директорию по указанному пути 
* echo # – может служить для записи строки в файл, если используется ‘>’ файл будет перезаписан, если ‘>>’ строка будет дописана в конец файла: echo "string" > filename

## Облегчает жизнь

* `apt install openssh` - в процессе, если потребуется, вводим ‘y’ 
* `pkill sshd` - этой командой останавливаем OpenSSH) 
* `termux-setup-storage` - подключить внутреннюю память 
* `cat ~/storage/downloads/termux.pub>>~/.ssh/authorized_keys` - копируем файл-ключ 
* `sshd` - запускаем ssh хост
* `apt install bash-completion` - Суть утилиты в том что, вводя команды вы можете нажав Tab воспользоваться автозаполнением.

Ну что за жизнь без текстового редактора с подсветкой кода (если вдруг захочется покодить, а оно захочется). Для установки пишем:

`apt install vim` - Тут уже можно пользоваться автозаполнением - пишем `apt i` теперь нажимаем Tab и наша команда дописывается до `apt install`

Пользоваться vim`ом не сложно, чтобы открыть файл 1.txt (если его нет, то он создастся) пишем:

```bash
vim 1.txt # Чтобы начать вводить текст нажмите ‘i’ 
#Чтобы закончить вводить текст нажмите ESC 
#Перед вводом команды должно быть двоеточие
‘:’ 
‘:q!’ – выйти без сохранения 
‘:w’ – сохранить # 
‘:wq’ – сохранить и выйти
```

## Пакет iproute2:

`pkg install iproute2`

После установки сможем вводить:

```bash
ifconfig -> ip address / ip a
route -> ip route / ip r
netstat -> ss
```