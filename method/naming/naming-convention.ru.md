# Соглашение по именованию

Для работы с [БЭМ-сущностями](../definitions/definitions.ru.md#БЭМ-сущность) необходимо ознакомиться с правилами их именования.

Основная идея соглашения по именованию — сделать имена CSS-селекторов максимально информативными и понятными. Это поможет [упростить разработку](../solved-problems/solved-problems.ru.md#Как-упростить-код-и-облегчить-рефакторинг) и [отладку](../solved-problems/solved-problems.ru.md#Как-начать-повторно-использовать-код-и-избежать-взаимного-влияния-компонентов-друг-на-друга) кода, а также решить некоторые [проблемы](../solved-problems/solved-problems.ru.md#Как-получить-самодокументируемый-код) веб-разработчиков.

В качестве примера рассмотрим CSS-селектор `menuitemvisible`. Быстрый просмотр такой записи не дает возможности определить типы БЭМ-сущностей по имени.

Добавим разделитель:

`menu-item-visible` или `menuItemVisible`

В таком виде имя селектора явно разделяется на логические части. Можем предположить, что `menu` окажется блоком, `item` — элементом, а `visible` — модификатором. Однако в реальной жизни часто возникают более сложные и не столь однозначные случаи, решить которые помогает соглашение по именованию БЭМ.

БЭМ-методология предоставляет идею по созданию правил формирования имен и свой способ ее реализации — [соглашение по именованию CSS-селекторов](#Соглашение-по-именованию-css-селекторов). Однако в мире веб-разработки существует ряд [альтернативных схем](#Альтернативные-схемы-именования), основанных на принципах БЭМ.

## Соглашение по именованию CSS-селекторов

* Имена БЭМ-сущностей записываются с помощью **цифр** и **латинских букв** в **нижнем регистре**.
* Для разделения слов в именах используется **дефис** (`-`).
* Для хранения информации об именах блоков, элементов и модификаторов используются **CSS-классы**.

Правила формирования имен:

* [блоков](#Имя-блока)
* [элементов](#Имя-элемента)
* [модификаторов](#Имя-модификатора)

### Имя блока

Имя блока формируется по схеме `block-name` и задает [пространство имен](https://ru.wikipedia.org/wiki/Пространство_имён) для элементов и модификаторов.

Иногда к именам блоков могут добавляться различные префиксы. Подробнее о нашем опыте использования префиксов рассказывается в статье [История создания БЭМ](https://ru.bem.info/method/history/#Появление-блоков).

**Пример**

`menu`

`lang-switcher`

*HTML*

```html
<div class="menu">...</div>
```

*CSS*

```css
.menu { color: red; }
```

### Имя элемента

Пространство имен, заданное именем блока, определяет принадлежность элемента к данному блоку. Имя элемента отделяется от имени блока двумя подчеркиваниями (`__`).

Полное имя элемента создается по схеме:

`block-name__elem-name`

Если блок имеет несколько одинаковых элементов, как в случае пунктов меню, то все они будут иметь одинаковые имена `menu__item`.

_________________________________________

**Важно!** В методологии БЭМ [не существует элементов элементов](../../faq/faq.ru.md#Почему-в-БЭМ-не-рекомендуется-создавать-элементы-элементов-block__elem1__elem2).
_________________________________________

**Пример**

`menu__item`

`lang-switcher__lang-icon`

*HTML*

```html
<div class="menu">
  ...
  <span class="menu__item"></span>
</div>
```

*CSS*

```css
.menu__item { color: red; }
```

### Имя модификатора

Пространство имен, заданное именем блока, определяет принадлежность модификатора к данному блоку или его элементу. Имя модификатора отделяется от имени блока или элемента одним подчеркиванием (`_`).

Полное имя модификатора создается по схеме:

* Для булевых модификаторов — `owner-name_mod-name`.

* Для модификаторов вида «ключ-значение» — `owner-name_mod-name_mod-val`.

_________________________________________________

**Важно!** В методологии БЭМ [модификатор не может использоваться в отрыве от своего владельца](../../faq/faq.ru.md#Зачем-писать-имя-блока-в-именах-модификаторов-и-элементов).
_________________________________________________

#### Модификатор блока

* **Булевый модификатор**.<br>
Значение такого модификатора не указывается. Полное имя создается по схеме:<br>
`block-name_mod-name`.<br>

**Пример**

    `menu_hidden`

* **Модификатор типа «ключ — значение»**.<br>
Значение модификатора отделяется от имени одним подчеркиванием (`_`). Полное имя создается по схеме:<br>
`block-name_mod-name_mod-val`.<br>

**Пример**

    `menu_theme_morning-forest`

*HTML*

```html
<div class="menu menu_hidden">...</div>
<div class="menu menu_theme_morning-forest">...</div>
```

>*Неверная форма записи*

>```html
<div class="menu_hidden">...</div>
>```

>В данном случае в записи отсутствует сам блок, на который влияет модификатор.

*CSS*

```css
.menu_hidden { display: none }
.menu_theme_morning-forest { color: green; }
```

#### Модификатор элемента

* **Булевый модификатор**.<br>
Значение такого модификатора не указывается. Полное имя создается по схеме:<br>
`block-name__elem-name_mod-name`.<br>

**Пример**

    `menu__item_visible`

* **Модификатор типа «ключ — значение»**.<br>
Значение модификатора отделяется от имени одним подчеркиванием (`_`). Полное имя создается по схеме:<br>
`block-name__elem-name_mod-name_mod-val`.<br>

**Пример**

    `menu__item_type_radio`

*HTML*

```html
<div class="menu">
  ...
  <span class="menu__item menu__item_visible menu__item_type_radio"></span>
</div>
```

*CSS*

```css
.menu__item_type_radio { color: blue; }
```

### Пример использования соглашения по именованию

Реализация формы аутентификации в HTML и CSS:

*HTML*

```html
<form class="form form_login form_theme_forest">
  <input class="form__input">
  <input class="form__submit form__submit_disabled">
</form>
```

*CSS*

```css
.form {}
.form_theme_forest {}
.form_login {}
.form__input {}
.form__submit {}
.form__submit_disabled {}
```

## Альтернативные схемы именования

Существуют альтернативные решения, основанные на соглашении по именованию БЭМ.

**Стиль Гарри Робертса**

Одним из первых, кто заговорил о БЭМ в англоязычном мире, был [Гарри Робертс](http://csswizardry.com/work/). В своей статье [MindBEMding&nbsp;–&nbsp;getting your head ’round BEM syntax](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) он рассказал о соглашении по именованию CSS-классов по БЭМ-методологии. Гарри Робертс предложил свою схему именования, основанную на принципах БЭМ:

`block-name__elem-name--mod-name`

* Имена записываются в нижнем регистре.
* Для разделения слов в именах БЭМ-сущностей используется дефис (`-`).
* Имя элемента отделяется от имени блока с помощью двух подчеркиваний (`__`).
* Булевые модификаторы отделяются с помощью двух дефисов (`--`).
* Модификаторы вида «ключ-значение» не используются.

**Стиль CamelCase**

`MyBlock__SomeElem_modName_modVal`

Данный стиль отличается от классического использованием [CamelCase](https://ru.wikipedia.org/wiki/CamelCase) вместо дефиса для разделения слов в именах БЭМ-сущностей.

**Стиль без подчеркиваний**

`blockName-elemName--modName--modVal`

* Для записи имен используется CamelCase.
* Имя элемента отделяется от имени блока с помощью одного дефиса (`-`).
* Для отделения модификатора используется два дефиса (`--`).
* Значение модификатора отделяется от его имени с помощью двух дефисов (`--`).

**Стиль No-namespace**

`_available`

Основное отличие данного стиля в отсутствии имени блока перед модификатором. Такая схема накладывает ограничения на испльзование [миксов](../definitions/definitions.ru.md#Микс), так как не дает возможности определить, к какому блоку относится модификатор.

## Какой стиль выбрать

Методология БЭМ предлагает общие принципы именования БЭМ-сущностей. Выбор схемы именования зависит от требований вашего проекта и личных предпочтений. Использование предложенного методологией [соглашения по именованию](#Соглашение-по-именованию-css-селекторов) имеет один существенный плюс — наличие готовых инструментов для разработки, которые ориентируются именно на «классическое именование».

Помимо этого, БЭМ-методология не ограничивается использованием технологий HTML и CSS, рассмотренных в этом документе. Понятия блоков, элементов и модификаторов применяются при работе с JavaScript, шаблонами и файловой системой БЭМ-проекта. Инструмент [bem-naming](https://ru.bem.info/tools/bem/bem-naming) позволяет применять одинаковые имена БЭМ-сущностей во всех используемых [технологиях реализации](../definitions/definitions.ru.md#Технология-реализации).

По умолчанию `bem-naming` содержит настройки соглашения по именованию, предложенного методологией, но позволяет добавлять правила для использования альтернативных схем.
