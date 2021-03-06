---
## Front matter
lang: ru-RU
title: Дискреционное разграничение прав в Linux. Основные атрибуты
author: |
	 НГУЕН ЧАУ КИ АНЬ  НБИбд-01-18\inst{1}

institute: |
	\inst{1}Российский Университет Дружбы Народов

date: 30 октября, 2021, Москва, Россия

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true

---

## Цель работы

Получение практических навыков работы в консоли с расширенными атрибутами файлов.

##  От имени пользователя guest определила расширенные атрибуты файла /home/guest/dir1/file1 командой lsattr /home/guest/dir1/file1

![Рис.1](image/001.png)

## Установила командой chmod 600 file1 на файл file1 права, разрешающие чтение и запись для владельца файла.


![Рис.2](image/002.png)

## 3. Попробовала установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest: chattr +a /home/guest/dir1/file1. В ответ получила отказ от выполнения операции.

![Рис.3](image/003.png)

## 4. Зашла на третью консоль с правами администратора, повысиласвои права с помощью команды su. Попробовала установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя:chattr +a /home/guest/dir1/file1

![Рис.4](image/004.png)

## 5. От пользователя guest проверяла правильность установления атрибута: lsattr /home/guest/dir1/file1

![Рис.5](image/005.png)

## 6. Выполнила дозапись в файл file1 слова «test» командой echo "test" /home/guest/dir1/file1

![Рис.6](image/006.png)

После этого выполнила чтение файла file1 командой cat /home/guest/dir1/file1

![Рис.7](image/007.png)

## 7. Попробовала удалить файл file1 либо стереть имеющуюся в нём информацию командой echo "abcd" > /home/guest/dirl/file1
![Рис.8](image/008.png)
Попробовала переименовать файл
![Рис.9](image/009.png)

## 8. Попробовала с помощью команды. При составлении работы использовались материалы [2—4]. chmod 000 file1 установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Не удалось выполнить указанные команды
![Рис.10](image/010.png)

##  9. Сняла расширенный атрибут a с файла /home/guest/dirl/file1 от имени суперпользователя командой chattr -a /home/guest/dir1/file1
![Рис.11](image/011.png)

## Повторила операции, которые ранее не удавалось выполнить.
![Рис.12](image/012.png)

## 10. Повторила действия по шагам, заменив атрибут «a» атрибутом «i». Не удалось ли вам дозаписать информацию в файл

![Рис.13](image/013.png)
![Рис.14](image/014.png)

## Сняла атрибут i
![Рис.15](image/015.png)

## Вывод

В результате выполнения работы я повысила свои навыки использования интерфейса командой строки (CLI), познакомилась на примерах с тем,
как используются основные и расширенные атрибуты при разграничении
доступа. Имела возможность связать теорию дискреционного разделения
доступа (дискреционная политика безопасности) с её реализацией на практике в ОС Linux. Составила наглядные таблицы, поясняющие какие операции возможны при тех или иных установленных правах. Опробовала действие на практике расширенных атрибутов «а» и «i».
