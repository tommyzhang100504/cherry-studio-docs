---
description: 数据设置→Obsidian配置
icon: gem
---

{% hint style="warning" %}
Этот документ переведен с китайского языка с помощью ИИ и еще не был проверен.
{% endhint %}

# Учебное руководство по настройке Obsidian

Cherry Studio поддерживает интеграцию с Obsidian, позволяя экспортировать как полные диалоги, так и отдельные сообщения в ваше хранилище Obsidian.

{% hint style="warning" %}
Для этого не требуется установка дополнительных плагинов Obsidian. Однако поскольку механизм экспорта Cherry Studio в Obsidian аналогичен принципу работы Obsidian Web Clipper, мы рекомендуем пользователям обновить Obsidian до последней версии (текущая версия должна быть не ниже **1.7.2**), чтобы избежать [сбоев импорта при экспорте длинных диалогов](https://github.com/obsidianmd/obsidian-clipper/releases/tag/0.7.0).
{% endhint %}

## Новое руководство

{% hint style="info" %}
По сравнению со старым методом экспорта в Obsidian, новая функция автоматически определяет путь к хранилищу, избавляя от необходимости вручную вводить название хранилища и папки.
{% endhint %}

### Шаг 1: Настройка Cherry Studio

Откройте Cherry Studio → _Настройки_ → _Настройки данных_ → _Конфигурация Obsidian_. В выпадающем списке автоматически отобразятся все открытые на вашем компьютере хранилища Obsidian. Выберите целевое хранилище:

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

### Шаг 2: Экспорт диалогов

#### Экспорт полного диалога

В интерфейсе диалогов Cherry Studio щелкните правой кнопкой мыши по диалогу, выберите _Экспортировать_ → _Экспортировать в Obsidian_:

<figure><img src="../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

Откроется окно для настройки **свойств заметки**, **местоположения папки** в Obsidian и **метода обработки**:

* **Хранилище**: выберите другое хранилище из выпадающего меню
* **Путь**: выберите папку для экспортируемой заметки
* Свойства заметки в Obsidian (Properties):
  * Теги (tags)
  * Дата создания (created)
  * Источник (source)
* **Методы обработки** при экспорте в Obsidian:
  * **Создать (перезаписать при наличии)**: создает новую заметку в указанной папке, перезаписывая существующую
  * **Добавить в начало**: добавляет содержимое диалога в начало существующей заметки
  * **Добавить в конец**: добавляет содержимое диалога в конец существующей заметки

{% hint style="info" %}
Свойства (Properties) экспортируются только при первом методе обработки.
{% endhint %}

<figure><img src="../.gitbook/assets/image (144).png" alt=""><figcaption><p>Настройка свойств заметки</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption><p>Выбор пути</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption><p>Выбор метода обработки</p></figcaption></figure>

После выбора всех параметров нажмите "ОК" для экспорта диалога в указанную папку хранилища Obsidian.

#### Экспорт отдельного сообщения

Для экспорта отдельного сообщения нажмите на _меню с тремя полосками_ под сообщением, выберите _Экспортировать_ → _Экспортировать в Obsidian_:

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption><p>Экспорт отдельного сообщения</p></figcaption></figure>

Откроется аналогичное окно для настройки **свойств** и **метода обработки**, как при экспорте полного диалога. Действуйте по инструкции [выше](obsidian.md#dao-chu-wan-zheng-dui-hua).

### Успешный экспорт

🎉 Поздравляем! Вы завершили настройку интеграции Cherry Studio с Obsidian и выполнили полный процесс экспорта. Наслаждайтесь!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Экспорт в Obsidian</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>Просмотр результата экспорта</p></figcaption></figure>



***

## Старое руководство (для Cherry Studio\<v1.1.13)

### Шаг 1: Подготовка Obsidian

Откройте хранилище Obsidian и создайте `папку` для экспортируемых диалогов (в примере используется папка Cherry Studio):

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

Запомните название `хранилища`, выделенное в нижнем левом углу.

### Шаг 2: Настройка Cherry Studio

В Cherry Studio → _Настройки_ → _Настройки данных_ → _Конфигурация Obsidian_ введите полученные на [Шаге 1](obsidian.md#di-yi-bu) название `хранилища` и `папки`:

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

Поле `Глобальные теги` необязательно – здесь можно указать теги для всех экспортируемых заметок.

### Шаг 3: Экспорт диалогов

#### Экспорт полного диалога

В интерфейсе диалогов щелкните правой кнопкой мыши по диалогу, выберите _Экспортировать_ → _Экспортировать в Obsidian_.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption><p>Экспорт полного диалога</p></figcaption></figure>

В открывшемся окне настройте **свойства заметки** и выберите **метод обработки**:
* **Создать (перезаписать при наличии)**: создает новую заметку в указанной папке
* **Добавить в начало**: добавляет контент в начало существующей заметки
* **Добавить в конец**: добавляет контент в конец существующей заметки

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption><p>Настройка свойств заметки</p></figcaption></figure>

{% hint style="info" %}
Свойства (Properties) экспортируются только при первом методе обработки.
{% endhint %}

#### Экспорт отдельного сообщения

Нажмите на _меню с тремя полосками_ под сообщением, выберите _Экспортировать_ → _Экспортировать в Obsidian_.

<figure><img src="../.gitbook/assets/image (141).png" alt=""><figcaption><p>Экспорт отдельного сообщения</p></figcaption></figure>

Действуйте по инструкции [выше](obsidian.md#dao-chu-wan-zheng-dui-hua) для настройки свойств и метода обработки.

### Успешный экспорт

🎉 Поздравляем! Вы завершили настройку интеграции Cherry Studio с Obsidian. Наслаждайтесь возможностями!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Экспорт в Obsidian</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>Просмотр результата экспорта</p></figcaption></figure>