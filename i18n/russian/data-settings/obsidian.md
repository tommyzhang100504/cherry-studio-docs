---
description: 数据设置→Obsidian配置
icon: gem
---

{% hint style="warning" %}
Этот документ переведен с китайского языка с помощью ИИ и еще не был проверен.
{% endhint %}

# Руководство по настройке Obsidian

Cherry Studio поддерживает интеграцию с Obsidian для экспорта полных диалогов или отдельных сообщений в ваше хранилище Obsidian.

{% hint style="warning" %}
Этот процесс не требует установки дополнительных плагинов Obsidian. Однако, поскольку механизм импорта Cherry Studio в Obsidian аналогичен Obsidian Web Clipper, рекомендуется обновить Obsidian до последней версии (текущая минимальная версия должна быть выше **1.7.2**), чтобы избежать [сбоев импорта при длинных диалогах](https://github.com/obsidianmd/obsidian-clipper/releases/tag/0.7.0).
{% endhint %}

## Новое руководство

{% hint style="info" %}
По сравнению со старой версией экспорта в Obsidian, новая функция позволяет автоматически выбирать путь к хранилищу, устраняя необходимость ручного ввода имени хранилища или папки.
{% endhint %}

### Шаг 1: Настройка Cherry Studio

Откройте в Cherry Studio _Настройки_ → _Настройки данных_ → меню _Конфигурация Obsidian_. В выпадающем списке автоматически появятся названия хранилищ Obsidian, ранее открытых на этом устройстве. Выберите целевое хранилище Obsidian:

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

### Шаг 2: Экспорт диалога

#### Экспорт полного диалога

Вернитесь в интерфейс диалогов Cherry Studio, щёлкните правой кнопкой мыши на диалоге, выберите _Экспорт_, затем нажмите _Экспортировать в Obsidian_:

<figure><img src="../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

Откроется окно для настройки **Свойств (Properties)** экспортируемой заметки, **расположения папки** в Obsidian и **метода обработки**:

* **Хранилище**: Выберите другое хранилище Obsidian из выпадающего меню
* **Путь**: Выберите папку для сохранения заметки из выпадающего меню
* Свойства заметки Obsidian:
  * Теги (tags)
  * Время создания (created)
  * Источник (source)
* Доступные **методы обработки**:
  * **Создать новый (перезаписать при существовании)**: Создаёт новую заметку в указанной папке **Путь**, перезаписывая существующую заметку с тем же именем
  * **Добавить в начало**: Добавляет экспортируемое содержимое диалога в начало существующей заметки с тем же именем
  * **Добавить в конец**: Добавляет экспортируемое содержимое диалога в конец существующей заметки с тем же именем

{% hint style="info" %}
Только первый метод включает Свойства (Properties), остальные два метода не включают их.
{% endhint %}

<figure><img src="../.gitbook/assets/image (144).png" alt=""><figcaption><p>Настройка свойств заметки</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption><p>Выбор пути</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption><p>Выбор метода обработки</p></figcaption></figure>

После выбора всех опций нажмите "ОК" для экспорта полного диалога в указанную папку хранилища Obsidian.

#### Экспорт отдельного сообщения

Для экспорта отдельного сообщения щёлкните на _меню с тремя полосками_ под сообщением, выберите _Экспорт_, затем нажмите _Экспортировать в Obsidian_:

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption><p>Экспорт отдельного сообщения</p></figcaption></figure>

Появится то же окно для настройки **Свойств заметки** и **Метода обработки**. Выполните действия, описанные в [руководстве по экспорту полного диалога](obsidian.md#dao-chu-wan-zheng-dui-hua).

### Успешный экспорт

🎉 Поздравляем! Вы завершили настройку интеграции Cherry Studio с Obsidian и выполнили весь процесс экспорта. Приятного использования!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Экспорт в Obsidian</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>Просмотр результатов экспорта</p></figcaption></figure>

***

## Старое руководство (для Cherry Studio<v1.1.13)

### Шаг 1: Подготовка Obsidian

Откройте хранилище Obsidian и создайте `папку` для сохранения экспортированных диалогов (например, папка "Cherry Studio" на изображении):

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

Запомните выделенный текст в нижнем левом углу — это имя вашего `хранилища`.

### Шаг 2: Настройка Cherry Studio

В Cherry Studio откройте _Настройки_ → _Настройки данных_ → меню _Конфигурация Obsidian_. Введите имя `хранилища` и `папки`, полученные на [Шаге 1](obsidian.md#di-yi-bu):

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

Поле `Глобальные теги` необязательно и позволяет задать теги для всех экспортируемых диалогов в Obsidian.

### Шаг 3: Экспорт диалога

#### Экспорт полного диалога

В интерфейсе диалогов Cherry Studio щёлкните правой кнопкой мыши на диалоге, выберите _Экспорт_, затем нажмите _Экспортировать в Obsidian_.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption><p>Экспорт полного диалога</p></figcaption></figure>

Откроется окно для настройки **Свойств (Properties)** заметки и выбора **метода обработки**:

* **Создать новый (перезаписать при существовании)**: Создаёт новую заметку в `папке`, указанной в [Шаге 2](obsidian.md#di-er-bu), перезаписывая существующую заметку
* **Добавить в начало**: Добавляет содержимое диалога в начало существующей заметки с тем же именем
* **Добавить в конец**: Добавляет содержимое диалога в конец существующей заметки с тем же именем

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption><p>Настройка свойств заметки</p></figcaption></figure>

{% hint style="info" %}
Только первый метод включает Свойства (Properties), остальные два метода не включают их.
{% endhint %}

#### Экспорт отдельного сообщения

Щёлкните на _меню с тремя полосками_ под сообщением, выберите _Экспорт_, затем нажмите _Экспортировать в Obsidian_.

<figure><img src="../.gitbook/assets/image (141).png" alt=""><figcaption><p>Экспорт отдельного сообщения</p></figcaption></figure>

Появится то же окно для настройки **Свойств заметки** и **Метода обработки**. Выполните действия, описанные в [руководстве по экспорту полного диалога](obsidian.md#dao-chu-wan-zheng-dui-hua).

### Успешный экспорт

🎉 Поздравляем! Вы завершили настройку интеграции Cherry Studio с Obsidian и выполнили весь процесс экспорта. Приятного использования!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Экспорт в Obsidian</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>Просмотр результатов экспорта</p></figcaption></figure>