---
layout: post
title: How to start
---

# TL;DR
Береш таск із дошки **ToDo/Major** на гітХабі. Присвоюєш його собі та перекидаєш на дошку **In progress**. Клонуєш собі на комп репозиторій проекту. Створюєш нову вітку. Робиш роботу. В останньому коміті прописуєш #**id** таска, наприклад. Пушиш свою вітку на гітХаб. Починаєш все спочатку.



## Code of Conduct
I don't care of your feeling.



## Tasks Managment
Поки що використовуємо *GitHub* та його можливості. До кожного проекту створюються наступні agile дошки:

- ToDo Candidates (всі можливі таски)
- Major Candidates  (пріоритетні таски)
- Problems (існуючі та потенційні проблеми)
- In progress (таски, над якими зараз ведеться робота)
- Done -> Achieved (завершені таски)

та теги:

- bug
- feature
- enhancement

Робочий процес відбувається за наступною схемою. Спочатку по ТЗ складається (приблизний) список всіх тасків по проекту. Далі вибираються найпріоритетніші таски, які треба реалізувати в першу чергу. Після цього член команди вибирає певний таск та починає над ним роботу.



## VSC Conventions
Використовуємо наступну схему вітвлення - [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/). Зміст якої полягає в розділенні стабільної версії проекту (вітка *master*) та версії яка активно змінюється (вітка *develop*). *Для кожного таску створюється окрема вітка. В останньому коміті цієї вітки пишеться #id* таска над яким велась робота.*Хорошим тоном вважаються маленькі коміти, які містять зміни файлів, що логічно об'єднані однією метою. Як правильно оформлювати повідомлення комітів описано [тут](https://slack-files.com/T2RPJSECR-F3185SHJ4-0c8db479f0).



## Code Conventions
В цілому код має відповідати [Java Code Conventions](http://www.oracle.com/technetwork/java/codeconventions-150003.pdf) із не значними змінами, описаними [тут](https://soft-g.slack.com/files/aint/F3185RAEL/code_conventions.md) *Але* якщо ми працюємо над legacy проектом, то щоб не вносити плутанини потрібно підлаштовуватися під наявний стиль коду.



## Stack of technologies
[Таблиця із фреймворками та технологіями](https://docs.google.com/spreadsheets/d/1dCswWH1h8umNRmAvwcpFZT2mcT6AJYbYwr-lCgkn_kc/edit#gid=0), які треба знати/вивчити. Такі базові речі, як основи Java/Web, упущені.



## Tools
Для уніфікації робочого процесу під Windows, використовуємо наступні тулзи:

- ConEmu (термінал для роботи із git)
- SmartGit (граф оболонка для git)
- Maven wrapper

та створюємо два файли в папці Windows користувача: - файл `.gitconfig`

```
[user]
   name = ім'я прізвище транслітом
   email = робочий емейл
[color]
   ui = true
[core]
   excludesfile = ~/.gitignore_global
   autocrlf = true
[credential]
   helper = cache --timeout=86400
```

- файл `.gitignore_global` можна скопіювати [звідси](https://github.com/aint/dotfiles/blob/master/.gitignore_global)

Налаштування для IntelliJ IDEA:

- Editor > Code Style Line separator : Unix and OS X (\n)
- Editor > Code Style > Java > Import Class count to use import with '*': 50
- Editor > Inspections > Raw use of Parameterized class
- Editor > Inspections > Serializable class without 'serialVersionUID'
