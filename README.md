### **Шпаргалка по написанию качественного кода**

Вопросы по ПХП:
1. Негласные правила именования переменной/функции/класса. 
2. Желательная длина функции. Почему?
3. Количество операций, выполняемых функцией. 
4. Аргументы функции.
5. Как писать “хорошие” функции?
6. Комментарии в программе.
7. Комментарии TODO.
8. Закомментированный код
9. Вертикальное форматирование кода.
10. Горизонтальное форматирование кода.
11. Антисимметрия данных(объектов).
12. Закон Деметры.
13. Объекты передачи данных (DTO).
14. Активные записи.
15. Обработка ошибок.
16. TDD. 3 закона TDD.
17. Структура тестов.
18. Характеристики тестов FIRST
19. Строение класса.
20. Принцип единой ответственности (SRP).
21. Четыре правила формирования архитектуры приложения.
22. Описать любой "неприятный запах" кода, и как его можно избежать.


**1. Именование переменных, функций и классов**
- **Переменные**: `snake_case` или `camelCase`, отражают суть данных.  
  Пример: `user_name`, `totalPrice`.  
- **Функции**: глаголы или действия, `snake_case`/`camelCase`.  
  Пример: `calculate_area()`, `send_email()`.  
- **Классы**: `CamelCase`, имена — существительные.  
  Пример: `Person`, `OrderProcessor`.

**2. Длина функции**
- Желательно **до 20-30 строк**.  
- Причина: легче читать, тестировать и поддерживать.

**3. Количество операций в функции**
- Функция должна выполнять **только одну задачу**.  
- Меньше операций — выше понятность и тестируемость.

**4. Аргументы функции**
- Оптимально: **1-3 аргумента**.  
- Если больше, используйте объекты или именованные параметры.

**5. Как писать хорошие функции?**
- Короткие, понятные, выполняющие одну задачу.  
- Чистые (без побочных эффектов).  
- Хорошо именованные и документированные.

**6. Комментарии в коде**
- Используйте для объяснения сложных мест.  
- Код должен быть **самодокументируемым**.

**7. Комментарии TODO**
- Используются для пометок о доработках.  
  Пример: `# TODO: добавить проверку ввода`.

**8. Закомментированный код**
- Избегайте. Если код не нужен — удалите.  
- Используйте систему контроля версий для хранения истории.

**9. Вертикальное форматирование**
- Разделяйте логические блоки пустыми строками.  
- Улучшает читаемость.

**10. Горизонтальное форматирование**
- Следите за длиной строки (не более 80-120 символов).  
- Выравнивайте аргументы и параметры.

**11. Антисимметрия данных**
- Структуры данных и объекты должны быть логично организованы.  
- Пример: не смешивайте данные и поведение в одном объекте.

**12. Закон Деметры**
- Объект знает только свои данные и данные объектов, переданных ему.  
- Это снижает зависимость и повышает модульность.

**13. Объекты передачи данных (DTO)**
- DTO содержат только данные, без логики.  
- Используются для передачи информации между слоями.

**14. Активные записи**
- Паттерн, где объект сам управляет своей персистентностью.  
- Пример: ORM-классы в Django, SQLAlchemy.

**15. Обработка ошибок**
- Используйте исключения для обработки ошибок.  
- Предоставляйте понятные сообщения.

**16. TDD (Test-Driven Development)**
- **1 закон**: сначала пишем тест.  
- **2 закон**: пишем код, чтобы тест прошел.  
- **3 закон**: рефакторим код без нарушения тестов.

**17. Структура тестов**
1. **Arrange**: настройка начальных условий.  
2. **Act**: выполнение тестируемого действия.  
3. **Assert**: проверка результата.

**18. Характеристики тестов (FIRST)**
- **F** — Fast (быстрые).  
- **I** — Independent (независимые).  
- **R** — Repeatable (повторяемые).  
- **S** — Self-validating (самопроверяемые).  
- **T** — Timely (своевременные).

**19. Строение класса**
- Конструктор инициализирует объект.  
- Методы выполняют операции.  
- Приватные и публичные члены.  
- Логичная структура.

**20. Принцип единой ответственности (SRP)**
- Класс выполняет одну задачу.  
- Изменяется по одной причине.

**21. Четыре правила архитектуры**
1. **Модульность**: независимые модули.  
2. **Слабая связанность**: минимальная зависимость.  
3. **Высокая когезия**: логическая связь внутри модуля.  
4. **Интерфейсы**: абстракции для взаимодействия.

**22. Неприятный запах кода: дублирование**
- **Как избежать**:  
  - Выделяйте повторяющийся код в функции или классы.  
  - Используйте шаблоны проектирования.


Вопросы по Тестированию:
1. Этапы разработки. Методологии. Роль тестирования в разработке.
2. Тестирование. Цели тестирования. Принципы тестирования
3. Этапы процесса тестирования. Критерии начала и окончания тестирования.
4. Классификация тестирования.
5. Требования
6. Причины ошибок. Дефект. Жизненный цикл дефекта.
7. Дефект. Приоритет и Серьезность.
8. Обеспечение качества.
9. Тест дизайн. Техники.
10. Тест-кейсы. Чек-листы.
11. Черный, Белый, Серый ящик.
12. Регрессия в тестировании.
13. Верификация и валидация.
14. Авторизация и аутентификация.
15. Протокол  HTTP. Клиент-серверная архитектура.
16. HTTP1/HTTP2. HTTPS.
17. AJAX.
18. HTML/CSS/JS.
19. Панель разработчика в браузере.
20. Инструменты тестирования.


###1. Этапы разработки. Методологии. Роль тестирования в разработке.
Этапы разработки:
•	Концепция
•	Договор
•	Требования / тз
•	Дизайн 
•	Разработка
•	Стабилизация
•	Релиз
•	Поддержка		
•	Закрытие проекта

Методологии разработки:
-Scrum (итерационная модель): Разработка делится на спринты (2-4 недели), каждый спринт — это завершенный цикл разработки. Задачи берутся из бэклога по приоритету.
-Waterfall (водопадная модель): Разработка делится на этапы, переход к следующему этапу возможен только после завершения предыдущего.
-Agile (гибкая модель): Все этапы выполняются одновременно, изменения вносятся на лету. Используется при ограниченном времени.

Роль тестирования:
-Тестировщик начинает работу на этапе требований, проверяя их полноту и непротиворечивость.
-На этапе разработки тестировщик создает стратегию тестирования, тест-кейсы, чек-листы и автоматизацию.
-На этапе закрытия проекта тестировщик проверяет полноту и правильность закрытия.

###2. Тестирование. Цели тестирования. Принципы тестирования.
Тестирование: *процесс проверки соответствия продукта требованиям.* Цель тестирования, как процесса – это повышение качества продукта.

Цели тестирования:
-Повышение качества продукта.
-Поиск, локализация и корректное описание багов.
-Обеспечение стабильной работы приложения с точки зрения заказчика и пользователя.

Принципы тестирования: 
•	Принцип присутствия дефекта, если вы протестировали функционал и не нашли в нем багов, это не значит, что в нем его нет
•	Принцип пестицида, способность багов адаптироваться к тестам, это значит, что необходимо модифицировать тесты, по мере развития кода.
•	Принцип раннего тестирования, стоимость исправления бага экспоненциально пропорциональна времени его обнаружении, то есть чем раньше и быстрее мы найдем баг и исправим, тем дешевле он обойдется.	
•	Принцип концентрации багов: 80% багов сконцентрировано в 20% приложения. ( основные главные места концентрация – это платформа apple, платежные системы и интеграция с любимы сторонними системами)

###3. Этапы процесса тестирования. Критерии начала и окончания тестирования.
Этапы:
1.	Общее планирование и анализ требований
2.	Уточнение критериев приемки. Этап на котором мы выясняем, что на самом деле хочет заказчик
3.	Уточнение стратегии тестирования
4.	Разработка тест-кейсов
5.	Выполнение тест-кейсов
6.	Фиксация найденных дефектов.
7.	Анализ результатов тестирования
8.	Отчетность
9.	Повтор цикла

Критерии начала тестирования:
-Наличие требований и ТЗ.
-Наличие готового функционала для тестирования.

Критерии окончания тестирования:
-Все тест-кейсы выполнены.
-Все найденные баги исправлены и проверены.
-Достигнуты критерии приемки.

###4. Классификация тестирования.
Упрощенная классификация:
-По запуску кода: статическое тестирование (без запуска кода) и динамическое тестирование.
-По доступу к коду: белый ящик (доступ к коду есть), черный ящик (доступа к коду нету), серый ящик (есть доступ к части кода).
-По степени автоматизации: ручное и автоматизированное.
-По уровню детализации приложения (тестирования): Модульное/компонентное, проверяются отдельно небольшие части приложения; Интеграционное, проверяется взаимодействие между несколькими частями приложения; Системное, приложение проверяется как единое целое.
-По убыванию степени важности тестируемых функций:
  1) Дымовое (smoke) тестирование - проверка самой ключевой функциональности, неработоспособность которой делает бессмысленное работу приложения
  2) Тестирование критического пути - проверка функциональности используемая типичным пользователем в типичной повседневной деятельности
  3) Расширенное тестирование - проверка всей остальной функциональности, заявленной в требовании
-По принципам работы с приложением: позитивное (взаимодействие с приложением осуществляется по инструкции) и негативное (используются некорректные данные, приводящие к ошибкам. Не предполагает корректную обработку данных).

Подробная классификация тестирования:
1.	Статическое тестирование:
a.	Документы
b.	Графические прототипы (дизайн)
c.	Код приложения
d.	Параметры
e.	Подготовленные тестовые данные

###5. Требования.

В требовании необходимо описывать то, что имеет значение для приложения или проекта. 
Источники и пути выявления требований:
•	Интервью. Интервью проводится с диктофоном, и все выписывается на документ.
•	Работа с фокусными группами, которые описываются в концепции.
•	Анкетирование. Необходимо учитывать, что какой-то процент анкетируемых проставит случайные ответы. 
•	Семинары и мозговой штурм.
•	Наблюдение. Очень важно фиксировать результаты наблюдений.
•	Прототипирование. Создание быстрого сырого приложения, которое имеет только необходимый функционал.
•	Анализ документов.
•	Моделирование процессов и их взаимодействие.
•	Самостоятельное описание. 
Прототипирование: оно проводится для проверки сомнительных частей программы, для которых есть некоторые неопределенности. 

Требования — это описание того, что должно быть реализовано в приложении. Тестировщик проверяет требования на:

Полноту: Исключение двоякого толкования.

Непротиворечивость: Отсутствие противоречий между требованиями.

###6. Причины ошибок. Дефект. Жизненный цикл дефекта.
Причины ошибок:
-Ошибки в требованиях.
-Ошибки в коде.
-Ошибки в интеграции компонентов.

Дефект — это расхождение между ожидаемым и фактическим результатом.

Жизненный цикл дефекта:
-Создан
-Запланирован
-Не выполнялся
-Выполняется
-Пропущен
-Провален
-Пройден успешно
-Заблокирован
-Закрыт
-Требует доработки

###7. Дефект. Приоритет и Серьезность.
Приоритет дефекта: Важность бага относительно функционала приложения.
Серьезность дефекта: Влияние бага на работу приложения.

###8. Обеспечение качества.
Обеспечение качества — это процесс, направленный на достижение стабильной работы приложения.
Включает:
-Тестирование.
-Регрессионное тестирование.
-Автоматизацию тестирования.
-Постоянное обновление тест-кейсов.

###9. Тест дизайн. Техники.
Тест дизайн — это процесс создания тест-кейсов.

Техники:
-Классы эквивалентности.
-Граничные значения.
-Причинно-следственный анализ.
-Таблицы решений.

###10. Тест-кейсы. Чек-листы.
Тест-кейс — это набор входных данных, условий выполнения и ожидаемых результатов для проверки функционала.

Чек-лист — это список того, что должно быть в приложении и работать.
Включает:
-Порядковый номер.
-Название требования.
-Приоритет.
-Возможное предусловие.

###11. Черный, Белый, Серый ящик.
Белый ящик: Тестирование с доступом к коду.

Черный ящик: Тестирование без доступа к коду.

Серый ящик: Тестирование с частичным доступом к коду.

###12. Регрессия в тестировании.
Регрессионное тестирование — проверка того, что ранее рабочий функционал не сломался после изменений. Проводится после добавления нового функционала.

###13. Верификация и валидация.
Верификация: Проверка соответствия продукта требованиям.

Валидация: Проверка, что продукт удовлетворяет потребностям пользователя.

###14. Авторизация и аутентификация.
Аутентификация: Процесс проверки личности пользователя (логин/пароль).

Авторизация: Процесс предоставления доступа к ресурсам после аутентификации.

###15. Протокол HTTP. Клиент-серверная архитектура.
HTTP — протокол передачи гипертекста между клиентом и сервером. Клиент отправляет запрос, сервер возвращает ответ.

Клиент-серверная архитектура: Клиент отправляет запросы, сервер обрабатывает их и возвращает ответы.

###16. HTTP1/HTTP2. HTTPS.
HTTP1: Одновременная обработка одного запроса.

HTTP2: Мультиплексирование, несколько запросов одновременно.

HTTPS: Защищенная версия HTTP с шифрованием данных.

###17. AJAX.
AJAX — технология, позволяющая обновлять данные на странице без её перезагрузки. Используется для асинхронных запросов.

###18. HTML/CSS/JS.
HTML: Язык разметки для создания структуры веб-страницы.

CSS: Язык стилей для оформления веб-страницы.

JS: Язык программирования для добавления интерактивности на веб-странице.

###19. Панель разработчика в браузере.

Панель разработчика позволяет:
-Просматривать и редактировать HTML/CSS.
-Отлаживать JavaScript.
-Анализировать сетевые запросы.
-Проверять производительность.

###20. Инструменты тестирования.
Selenium: Для автоматизации тестирования веб-приложений.

Postman: Для тестирования API.

Jenkins: Для автоматизации сборки и тестирования.

Jira/Redmine: Для управления задачами и баг-трекинга.
