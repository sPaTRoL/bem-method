# Проекты на БЭМ

В этом разделе мы собрали полезные и интересные проекты на БЭМ.

Если вашего проекта еще нет в этом разделе, напишите нам на [info@bem.info](mailto:info@bem.info).

## bem-flashcards

Небольшой проект на основе project-stub с использованием библиотек bem-core и bem-history. Содержит набор английских слов с переводом, которые выводятся в виде переворачивающихся карточек. Есть возможность заменить словарь на другой или просто на произвольный набор пар фраз.

Для подготовки словаря из XLS-файла есть [ruby-скрипт](https://gist.github.com/ololobus/11f222d1fc48f2efef56). Входной XLS-файл должен содержать три колонки (A, B, C): слово, транскрипция, перевод.

Проект готов к использованию. Форкайте, меняйте и дополняйте словарь.

Репозиторий проекта на [GitHub](https://github.com/ololobus/bem-flashcards/), [демонстрация](http://ololobus.github.io/bem-flashcards).

Автор проекта — Алексей Кондратов, [gh: ololobus](https://github.com/ololobus), [@ololobuss](https://twitter.com/ololobuss), [kondratov.aleksey@gmail.com](mailto:kondratov.aleksey@gmail.com).

## bem-grid

Библиотека для описания CSS-сеток. CSS-сетка построена на flexbox'ах и имеет деградацию для старых браузеров, а также она полностью настраивается под любые нужды через переменные, используют rem единицы и суперскоростной Stylus. Основана на библиотеке bem-core.

Репозиторий проекта на [GitHub](https://github.com/verybigman/bem-grid).

Автор проекта — Антон Виноградов, [gh: verybigman](https://github.com/verybigman), [@awinogradov](https://twitter.com/awinogradov), [winogradovaa@gmail.com](mailto:winogradovaa@gmail.com).

## bem-ng

Библиотека для совместного использования БЭМ-методологии и AngularJS. Позволяет писать view-ориентированный BEMJSON.

Репозиторий проекта на [GitHub](https://github.com/verybigman/bem-ng).

Автор проекта — Антон Виноградов, [gh: verybigman](https://github.com/verybigman), [@awinogradov](https://twitter.com/awinogradov), [winogradovaa@gmail.com](mailto:winogradovaa@gmail.com).

## bemy

Приложение на Node.js для манипуляций с БЭМ-структурой. Позволяет создавать и переименовывать БЭМ-сущности в файловой системе (аналог команды `bem create`). Умеет создавать файловую структуру блока по `deps.js`-файлам сборщика [ENB](http://enb-make.info). Интегрируется посредством командной строки в Webstorm, Sublime и другие редакторы.

Репозиторий проекта на [GitHub](https://github.com/f0rmat1k/bemy).

Автор проекта — Антон Грищенко, [gh: f0rmat1k](https://github.com/f0rmat1k), [f0rmateg@yandex.ru](mailto:f0rmateg@yandex.ru).

## generator-bem-ng

Необыкновенный генератор БЭМ-проектов, использующих AngularJS. С ним вы сможете создать базовую структуру БЭМ-проекта и модули AngularJS приложения. Генератор использует непривычную, на первый взгляд, парадигму модулей, но очень удобную и правильную для тех, кто знаком с БЭМ.

Репозиторий проекта на [GitHub](https://github.com/verybigman/generator-bem-ng).

Автор проекта — Антон Виноградов, [gh: verybigman](https://github.com/verybigman), [@awinogradov](https://twitter.com/awinogradov), [winogradovaa@gmail.com](mailto:winogradovaa@gmail.com).

## gem 'bem-on-rails’

Позволяет работать с БЭМ-методологией в проектах на Ruby on Rails.

Репозиторий проекта на [GitHub](https://github.com/verybigman/bem-on-rails).

Автор проекта — Антон Виноградов, [gh: verybigman](https://github.com/verybigman), [@awinogradov](https://twitter.com/awinogradov), [winogradovaa@gmail.com](mailto:winogradovaa@gmail.com).

## atom-bemjson-snippets

Набор сниппетов для быстрого набора BEMJSON в свободном редакторе Atom. Устанавливается из менеджера пакетов Atom.

Репозиторий проекта на [GitHub](https://github.com/verybigman/atom-bemjson-snippets)

Автор проекта — Антон Виноградов, [gh: verybigman](https://github.com/verybigman), [@awinogradov](https://twitter.com/awinogradov), [winogradovaa@gmail.com](mailto:winogradovaa@gmail.com).

## bem-social

Библиотека блоков социальных виджетов для сайтов, использующих БЭМ-стек технологий. Share, Like, Follow, Yandex.Share API и другие. Содержит SVG-иконки социальных сетей и несколько тем оформления. Библиотека использует некоторые блоки библиотеки [bem-components](https://ru.bem.info/libs/bem-components/).

Репозиторий проекта на [GitHub](https://github.com/voischev/bem-social)

Автор проекта — Иван Воищев, [gh: voischev](https://github.com/voischev), [@voischev](https://twitter.com/voischev), [voischev.ivan@ya.ru](mailto:voischev.ivan@ya.ru).

## bnsf

Фреймворк для создания одностраничных приложений по методологии БЭМ. Позволяет легко использовать единожды написанный код, в первую очередь шаблоны и маршрутизацию, как на клиенте, так и на сервере. Дружелюбен к поисковым системам. Зависит от [bem-core](https://ru.bem.info/libs/bem-core), для шаблонизации использует `BEMHTML` и `BEMTREE`, сборка через `bem-tools`.

Репозиторий проекта на [GitHub](https://github.com/apsavin/bnsf)

Автор проекта — Александр Савин, [gh: apsavin](https://github.com/apsavin), [@apsavin](https://twitter.com/ap_savin), [a.p.savin@yandex.ru](mailto:a.p.savin@yandex.ru).

## sails-bem-project-stub

Заготовка проекта на nodejs MVC-фреймворке [Sails](http://sailsjs.org).

В качестве фронтенда используется полный стек технологий БЭМ: BEMTREE, BEMHTML, i-bem.js, библиотеки bem-core и bem-components. БЭМ-блоки интерфейса находятся в папке views.

Проект настроен на использование mongoDB, но предоставляет возможность использовать произвольную базу данных.

Репозиторий проекта на [GitHub](https://github.com/alexbaumgertner/sails-bem-project-stub).

Автор проекта — Александр Баумгертнер, [gh: alexbaumgertner](https://github.com/alexbaumgertner), [@alexbaumgertner](https://twitter.com/alexbaumgertner), [alexbaumgertner@yandex.ru](mailto:alexbaumgertner@yandex.ru).

## bem-site-engine

Проект для сбора и публикации документации, основанный на использовании библиотеки `bem-core@v2*`. Предназначен для запуска сайта с набором статей, представленном в удобном для навигации и поиска виде.

В проекте используются блоки из библиотеки [bem-components](https://ru.bem.info/libs/bem-components/). Более подробно про проект рассказывается в [докладе](https://events.yandex.ru/lib/talks/2191/) на BEMup'е в Санкт-Петербурге.

На данный момент ветка dev стабилизирована и заморожена для разработки. Баги принимаем в [issues](https://github.com/bem/bem-site-engine/issues) проекта на GitHub.

Репозиторий проекта на [GitHub](https://github.com/bem/bem-site-engine).

Автор проекта –  Андрей Кузнецов, [gh: tormozz48](https://github.com/tormozz48), [@kuznetsov48](https://twitter.com/@kuznetsov48), [andrey.kuznetsov48@yandex.ua](mailto:andrey.kuznetsov48@yandex.ua).

___________________________________
**Присоединяйтесь и вы!**
