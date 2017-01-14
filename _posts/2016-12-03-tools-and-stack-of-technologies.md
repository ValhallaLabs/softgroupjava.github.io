---
layout: post
title: Tools & Stack of technologies
---

## Stack of technologies

[Таблиця із фреймворками та технологіями](https://docs.google.com/spreadsheets/d/1dCswWH1h8umNRmAvwcpFZT2mcT6AJYbYwr-lCgkn_kc/edit#gid=0), які треба знати/вивчити. Такі базові речі, як основи Java/Web, упущені.

## Tools

Для уніфікації робочого процесу під Windows, використовуємо наступні тулзи:

 - ConEmu (заміна стандартного термінала)
 - git gui, gitk / SmartGit
 - Maven Wrapper
 - mindmup.com (візуалізація схем, структур)

Створюємо два файли в папці Windows користувача:

 - файл ```.gitconfig```
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
 - файл ```.gitignore_global``` можна скопіювати [звідси](https://github.com/aint/dotfiles/blob/master/.gitignore_global)

Налаштування для IntelliJ IDEA:

 - Editor > Code Style Line separator : Unix and OS X (\n)
 - Editor > Code Style > Java > Import Class count to use import with '*': 50
 - Editor > Inspections > Raw use of Parameterized class
 - Editor > Inspections > Serializable class without 'serialVersionUID'
