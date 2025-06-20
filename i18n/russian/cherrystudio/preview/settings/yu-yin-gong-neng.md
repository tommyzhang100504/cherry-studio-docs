---
hidden: True
icon: phone-arrow-up-right
---

{% hint style="warning" %}
Этот документ переведен с китайского языка с помощью ИИ и еще не был проверен.
{% endhint %}

```markdown
# Голосовые функции

```
Инструкция по использованию голосовых функций Cherry Studio

1. Обзор голосовых функций

Cherry Studio предлагает три модуля голосовых функций: TTS (текст-в-речь), ASR (распознавание речи) и голосовые вызовы. Эти функции позволяют общаться с ИИ естественным образом с помощью голоса, улучшая пользовательский опыт.

- TTS (текст-в-речь): преобразует текстовые ответы ИИ в голос
- ASR (распознавание речи): преобразует ваш голос в текст
- Голосовые вызовы: комбинация TTS и ASR для голосового диалога, как в ChatGPT

2. Функция TTS (текст-в-речь)

1. Поддерживаемые сервисы

Cherry Studio поддерживает четыре типа TTS-сервисов:

- OpenAI: использует OpenAI TTS API, требует API ключ
- Браузерный TTS: использует встроенную функцию браузера, бесплатно, без настройки
- Siliconflow: использует сервис Siliconflow, требует API ключ
- Бесплатный онлайн TTS: не требует API ключа

2. Настройка

1) Перейдите в настройки, выберите вкладку "Голосовые функции"
2) В подвкладке "TTS":
   - Включите TTS (переключатель)
   - Выберите тип TTS-сервиса
   - Заполните параметры в зависимости от выбранного сервиса:
     - OpenAI: API ключ, API адрес, выбор голоса и модели
     - Браузерный TTS: выбор голоса
     - Siliconflow: API ключ, API адрес, выбор голоса, модели, формата ответа и скорости речи
     - Бесплатный онлайн TTS: выбор голоса и выходного формата
3) Настройте опции фильтрации TTS (опционально):
   - Фильтровать мыслительные процессы
   - Фильтровать Markdown-разметку
   - Фильтровать блоки кода
4) Настройте отображение индикатора воспроизведения
5) Нажмите "Проверить TTS" для тестирования

3. Использование

- При включенном TTS ответы ИИ автоматически озвучиваются
- Кнопка воспроизведения отображается под каждым ответом ИИ
- Клик на кнопке: воспроизведение/пауза
- Индикатор прогресса отображается при включении
- Длинные тексты сегментируются и воспроизводятся последовательно

3. Функция ASR (распознавание речи)

1. Поддерживаемые сервисы

Доступны три типа ASR-сервисов:

- OpenAI: использует модель Whisper, требует API ключ
- Браузерный: встроенная функция браузера, бесплатно
- Локальный сервер: подключение к локальному WebSocket-серверу

2. Настройка

1) Перейдите в настройки, выберите вкладку "Голосовые функции"
2) В подвкладке "ASR":
   - Включите ASR (переключатель)
   - Выберите тип ASR-сервиса
   - Заполните параметры:
     - OpenAI: API ключ, API адрес, выбор модели
     - Браузерный: без настройки
     - Локальный сервер: автоматический запуск при старте приложения
   - Выберите язык распознавания (по умолчанию: китайский)
3) Нажмите "Проверить ASR" для тестирования

3. Использование

- Кнопка распознавания появляется рядом с полем ввода
- Клик для начала записи
- Речь преобразуется в текст и вставляется в поле ввода
- Повторный клик - остановка записи
- Режим непрерывного распознавания с накоплением текста

4. Функция голосовых вызовов

1. Особенности

- Полноценный голосовой диалог (TTS + ASR)
- Перемещаемое плавающее окно
- Режим "Удерживать для разговора"
- Настройка горячих клавиш
- Сворачивание окна
- Выбор специализированной модели
- Настройка промптов

2. Настройка

1) Перейдите в настройки, выберите вкладку "Голосовые функции"
2) В подвкладке "Голосовые вызовы":
   - Включите функцию (переключатель)
   - Нажмите "Выбрать модель" для выбора модели ИИ
   - Настройте промпты в текстовом поле (опционально)
   - Сохраните или сбросьте до стандартных

3. Использование

1) Нажмите иконку телефона справа от поля ввода
2) Откроется окно вызова с приветствием
3) Удерживайте кнопку "Говорить" для записи (или горячую клавишу)
4) Отпустите для отправки голоса ИИ
5) ИИ отвечает через TTS
6) Управление кнопками:
   - Отключение звука
   - Пауза/продолжение
   - Настройка горячих клавиш
   - Сворачивание окна
7) Закрытие - кнопка "Закрыть"

4. Настройка горячих клавиш

1) В окне вызова нажмите иконку настроек
2) В панели нажмите "Горячие клавиши"
3) Нажмите нужную клавишу (пробел, Shift и др.)
4) Сохраните настройку
5) Используйте: удерживайте клавишу для записи, отпустите для отправки

5. Частые проблемы и решения

1. Проблемы с TTS

- Нет звука: проверьте включение, настройки сервиса
- Плохое качество: смените сервис/голос
- Ошибки: проверьте API ключ и интернет-соединение

2. Проблемы с ASR

- Не распознается речь: проверьте включение и настройки
- Низкая точность: смените сервис, настройте микрофон
- Ошибка подключения: проверьте локальный сервер/перезапуск

3. Проблемы с вызовами

- Окно не открывается: проверьте включение функции и настройки TTS/ASR
- Нет реакции на запись: проверьте разрешения микрофона
- Нет озвучки ответов: проверьте TTS и включение звука

6. Расширенные настройки

1. Расширенные настройки TTS

- Фильтрация: мыслительные процессы, Markdown, блоки кода
- Индикатор прогресса
- Кастомные голоса и модели

2. Расширенные настройки ASR

- Автозапуск сервера
- Выбор языка

3. Расширенные настройки вызовов

- Кастомные промпты
- Выделенная модель ИИ
- Настройка горячих клавиш

7. Рекомендации

1. Выбор TTS:
   - Качество: OpenAI/Siliconflow
   - Простота: браузерный/бесплатный TTS

2. Выбор ASR:
   - Точность: OpenAI
   - Простота: браузерный

3. Оптимизация вызовов:
   - Используйте наушники
   - Тихое окружение
   - Кастомные промпты

4. Гибкая настройка:
   - Только TTS для текстового общения
   - Только ASR для голосового ввода
   - Полный голосовой диалог по необходимости

Надеемся, инструкция поможет полностью использовать голосовые функции Cherry Studio для естественного общения с ИИ!
```