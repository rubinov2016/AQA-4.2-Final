# План тестирования записи на курс "Тестировщик ПО"

# Перечень автоматизируемых сценариев

Разработка автоматизируемых сценариев планируется на уровне модульного тестирование (тестирование модуля "запись на обучение профессии "Тестировщик ПО")

    Виды тестирования
    - функциональное на соответствие требования
    - тестирование пользовательского интерфейса
    
    Будет тестироваться корректность 
    - перехода к форме записи на курс через главную страницу и все возможные интерфейсы
    - заполнения формы записи на курс
    - исполнения формы записи на курс

## 1. Позитивные сценарии

**1.1 Переход к форме записи на курс**

***Входные данные/предусловие***

Вход на главную страницу [сайт Нетологии](https://netology.ru)

***Шаги***

    Первый сценарий
    Шаг 1
    - выбрать группу "Программирование"
    - ИЛИ выбрать иконку "НЕО для начинающих"
    Шаг 2
    - выбрать "Тестировщик ПО"

    Второй сценарий
    Шаг 1
    - выбрать опцию "Каталог курсов"
    Шаг 2
    - выбрать группу "Программирование"  
    - ИЛИ выбрать "Полный каталог", строка Поиск
    Шаг 3 
    - выбрать "Тестировщик ПО"

***Ожидаемый результат***

Переход на страницу [Запись на курс](https://netology.ru/programs/qa)

**1.2 Заполнение формы записи на курс**

***Входные данные/предусловие***

Вход на страницу [Запись на курс](https://netology.ru/programs/qa)

***Шаги***

    Первый сценарий без входа в свой аккаунт
    Шаг 1 
    - Выйти из своего аккаунта, есть ранее вошли в систему
    Шаг 2
    - Нажать кнопку "Записаться" в начале страницы.  
    - ИЛИ нажать кнопку "Записаться" в блоке "Гарантия возврата денег". 
    - ИЛИ заполнить поля контактов в блоке "Запишитесь или получите консультацию". 
    Шаг 3
    - Заполнение формы корректными значениями

    Второй сценарий со входом в свой аккаунт
    Шаг 1
    - Войти в свой аккаунта, есть ранее вошли не в систему
    Шаг 2
    - Нажать кнопку "Записаться" в начале страницы.
    Шаг 3
    - Заполнение формы корректными значениями 

***Ожидаемый результат***

    Cообщение об успешной отправке формы

## 2. Негативные сценарии

**2.1 Некорректный поиск курса**

***Входные данные/предусловие***

Вход на страницу [Запись на курс](https://netology.ru/navigation) 

***Шаги***

    Шаг 1
    - Выбор поля Поиск
    Шаг 2
    - Ввод последовательности символов, отсутствующих в строке "Тестировщик ПО"

***Ожидаемый результат***

    Отсутствие возможности выбора курса "Тестировщик ПО"

**2.2 Заполнение формы записи на курс**

***Входные данные/предусловие***

Вход на страницу [Запись на курс](https://netology.ru/programs/qa)

***Шаги***

    Шаг 1
    - Проверка валидации поля Имя, ввод цифр
    Шаг 2 
    - Проверка валидации поля Телефон, ввод латинских символов
    Шаг 3 
    - Проверка валидации поля Электронная почта, ввод кириллических символов

***Ожидаемый результат***

Сообщение об ошибке валидации внизу поля, написанное красным цветом  

# Перечень используемых инструментов с обоснованием выбора

- GitHub: система контроля версий и веб-сервис для хостинга IT-проектов. Автоматический запуск тестов при совершении
  новых коммитов.
- IntelliJ IDEA: одна из наиболее удобных современных сред разработки программного обеспечения
- Gradle: инструмент сборки и запуска тестов. Специально разработан для описания сборки, тестирования, развертывания,
  экспорта
- Java: один из самых популярных языков программирования для реализации тестов.
- JUnit5: библиотека для модульного тестирования программного обеспечения
- Selenide: фреймворк для автоматизированного тестирования веб-приложений
- Allure: фреймворк для создания отчетов

# Перечень необходимых разрешений/данных/доступов

При наличии тестовой системы
- Доступ/разрешение к тестовой системе/SUT
- Набор тестовых данных (наполнение сайта), максимально приближенный в рабочему сайту
  
При отсутствии тестовой системе
- Разрешение на автоматизированное тестирование на рабочем сайте

# Перечень и описание возможных рисков при автоматизации

- Невыявление всех ошибок в коде или настройках окружения
- Неправильная оценка трудозатрат по тестированию
- Неполные или некорректные тестовые данные
- Ошибки при работе с рабочим сайтом, которые вызывают избыточную нагрузку
- Сложности реализации формы, нечитаемоcть кода (отсутствие локаторов и прочее)

# Перечень необходимых специалистов для автоматизации

- Тестировщик для написания и запуска автотестов
- Системный администратор для настройки тестового окружения

# Интервальная оценка с учётом рисков (в часах)

- Создание детального плана тестирования и техзадания - 3 часа
- Написание автотестов - 15 часов
- Настройка тестового окружения и тестовых данных - 3 часа
- Запуск автотеста, проверка отчетов, занесение результатов запуска в протокол и баг-репорты (github) – 5 часов

