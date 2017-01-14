---
layout: post
title: Git Conventions
---

Використовуємо наступну схему вітвлення - [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/). Зміст якої полягає в розділенні стабільної версії проекту (вітка *master*) та версії яка активно змінюється (вітка *develop*). **Для кожного таску створюється окрема вітка, в назві якої міститься  #**id** таска над яким ведеться робота.** Наприклад `issue_#42`.

Хорошим тоном вважаються маленькі коміти, які містять зміни файлів, що логічно об'єднані однією метою. Як правильно оформлювати повідомлення комітів описано [тут](http://chris.beams.io/posts/git-commit/) та нище.

Повідомлення коміта складається із заголовка та тіла. Команда `git commit -m "message"` робить коміт лише із заголовком.

- використовуємо стандартне правило 50/72
- перший рядок містить загальний опис зробленого в коміті, __не більше 50 символів__
- якщо зроблене в коміті не можна виразити одним чітким реченням, тоді після заголовку робиться пустий рядок, а далі йде детальний опис, __не більше 72 сивола в рядку__

#### Example
```
Add interface for plugins that to handle HTTP requests

All plugins that implement WebControllerPlugin interface can process
http requests:
- Plugin generates html code that will be inserted in the template
 ("plugin/plugin.jsp").
- Plugin should specify the subPath for requests it processes

All logic for searching proper plugin for the request is located in the
PluginController.
```
