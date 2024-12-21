# **Aviasales на минималках**

Наш проект **"Aviasales на минималках"** - это веб-сервис, который позволяет пользователям искать авиабилеты, сохранять свои предпочтения и получать уведомления об интересующих направлениях. 

---

## **Функционал**

- **Поиск авиабилетов:**  
  Пользователь вводит города вылета и прилета, соответствующие даты и максимальную цену, а система выводит подходящие варианты.
  
- **Регистрация и личный кабинет:**  
  Каждый пользователь может зарегистрироваться, сохранить свои предпочтения и управлять подписками на интересующие направления.

- **Парсинг данных:**  
  Автоматический сбор информации с сайтов авиакомпаний и агрегаторов билетов, чтобы всегда предлагать актуальные цены.

- **Уведомления:**  
  Если билеты удовлетворяют запросам пользователя, система отправляет уведомление по электронной почте.

---

## **Архитектура проекта** (на данный момент*)

Проект разделён на несколько компонентов, организованных по файлам и папкам:
Основные файлы проекта:

    README.md
    Документация по проекту. 

    .gitignore
    Файл, исключающий временные и ненужные файлы из контроля версий.

    requirements.txt
    Список всех зависимостей, необходимых для работы приложения.

    src/
    Директория, содержащая все файлы для работы сервиса.

        app.py
        Главный файл приложения, запускающий сервер Flask. В нём находятся маршруты для обработки запросов:
            / — главная страница с формой поиска.
            /search — обработка поисковых запросов.
            /profile — личный кабинет пользователя.
            /signup - регистрация нового пользователя.
            /login - авторизация пользователя.
            /logout - выход из личного кабинета.
    
        resources/
        Директория для ресурсов (HTML-шаблоны и база данных пользователей)

            user.db - база данных зарегистрированных пользователей
        
            templates/
            Директория для HTML-шаблонов:
                  login.html — страница авторизации.
                  main.html - страница поиска билетов.
                  profile.html — страница личного кабинета пользователя.
                  signup.html — страница регистрации.
                  results.html - страница с результатами поиска.

        parser/
        Директория с парсером

            parser_aeroflot.py
            Парсер сайта aeroflot.ru

        tests/
        Директория для тестирование сервисов

            test_app.py
            Тесты, проверяющие работу сервиса.



## **Технологии**

- **Бэкенд:** Python (Flask)
- **Фронтенд:** HTML, CSS (Jinja2 для шаблонов)
- **Данные:** Храним предпочтения пользователей и результаты парсинга в кэше
- **Парсинг:** Python (библиотекa Selenium)
- **Планировщик задач:** `crontab` для регулярного обновления данных

---

## **Установка и запуск**

### **Шаг 1: Клонирование репозитория**
```bash
git clone https://github.com/ваш_репозиторий/aviasales.git
cd aviasales
```

### **Шаг 2: Настройка виртуального окружения**
```bash
python3 -m venv .venv
source .venv/bin/activate   # Linux/MacOS
.venv\Scripts\activate      # Windows
```

### **Шаг 3: Установка зависимостей**
```bash
pip install -r requirements.txt
```

### **Шаг 4: Запуск приложения**
```bash
flask run
```

Приложение будет доступно по адресу: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## **Использование**

### **Главная страница**
1. Введите место назначения и максимальную цену.
2. Нажмите "Искать", чтобы увидеть список билетов.

### **Личный кабинет**
- Перейдите в личный кабинет по ссылке на главной странице.
- Управляйте своими подписками и настройками.

---

## **Команда проекта**

- **Джалилова Амина**: Фронтенд + Бэкенд (+ сборка)
- **Кашникова Ксения**: Фронтенд + Парсер (+ тестирование)
- **Попова Анна (@ya1ek)**: Фронтенд + Бэкенд (+ тестирование)

---

## **Планы по развитию**

1. Улучшение интерфейса личного кабинета.
2. Добавление функции фильтрации по времени вылета.
3. Интеграция с API авиакомпаний для ещё более точных данных.
4. Уведомления через мессенджеры (Telegram, WhatsApp).

---

## **Контакты**

Если у вас есть вопросы или предложения, свяжитесь с нами:  
📧 **ya1ek**: [Telegram](https://t.me/ya1ek)

---

Спасибо, что выбрали **Aviasales на минималках**! ✈️  
Ваши путешествия начинаются здесь. 🚀
