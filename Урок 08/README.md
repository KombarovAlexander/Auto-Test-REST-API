## **Коллекция ДЗ Урок 8.** Функции JavaScript

#### Задание 36.

Дана строка:

``` javascript
let mar = 'море, море, океан, море, море, яхта';

 ```

Получить массив, в котором будут храниться все позиции (индексы), с которых подстрока "_**море**_" входит в исходную строку. Сформированный массив вывести в консоль.

##### Запрос задания:

- **GET ДЗ 36 Работа со строкой Консоль**
    

#### Задание 37.

**DADATA**, поиск по фамилии. Отправить ресурсу **DADATA** запрос, тело которого имеет вид:

``` json
{
  "query": "Ан"
}

 ```

На основе полученного ответа от сервера создать 3 массива, в которых должны содержаться:

- _**surname_arr**_ - фамилии
- _**name_arr**_ - имена
- _**patronymic_arr**_ - отчества
    

Полученные массивы вывести в консоль. Массивы не должны содержать пустых значений, только действительные.

##### Запросы задания:

- **POST ДЗ 37 DADATA Поиск по фамилии Результаты ответа в массив**
    

#### Задание 38.

**JIRA**, метод _**getIssue**_. Обратиться к задаче _**TV-4**_ и получить дату ее создания. Проверить полученную дату на соответствие. Проверку провести двумя с пособами:

- с помощью метода _**toDateString()**_
- с помощью библиотеки _**moment**_
    

##### Запросы задания:

- **GET ДЗ 38 JIRA getIssue Работа с датами Moment**
    

#### Задание 39.

**USERS**, метод _**addTaskInCron**_. Отправить на ресурс **USERS** запрос, добавляющий созданную ранее задачу в расписание. Тело запроса имеет следующий вид:

``` json
{
    "email_owner": emailOwner,
    "task_id": idTask,
    "hours": 14,
    "minutes": 23,
    "month": 3,
    "days": 30,
    "day_weeks": 0
}

 ```

Написать автотесты, проверяющие, что:

- В ответе сервера присутствует свойство **type** и его тип - _**строка**_.
- Свойство **type** имеет значение _**success**_.
- Свойство **message** содержит подстроки "_**Расписание успешно добавлено в задачу**_" и "_**Следущая дата запуска**_".
- **Дата следующего запуска** задачи соответствует указанной при ее добавлении в расписание.
    

##### Запросы задания:

- **POST ДЗ 39 USER addTaskInCron Добавление задачи в расписание**
    

##### Примечание:

1. Необходимые для запроса сущности - _**пользователь**_, _**компания**_ и _**задача**_ - были созданы в _**Pre-request Script**_'е запроса с помощью метода _**sendRequest()**_ объекта **pm**.
2. При передаче даты следующего запуска задачи не указывается год. Он вычисляется системой, исходя из того, в каком году число и месяц будут соответствовать определенному дню недели. Для вычисления года даты по имеющимся числу, месяцу и дню недели была реализована функция _**setDate()**_.
3. В функции _**setDate()**_ используется библиотека **moment**.
    

#### Задание 40.

**SHOP,** метод _**search**_. В _**Pre-request Script**_'е запроса с помощью метода _**sendRequest()**_ объекта **pm** создать _**рандомное**_ количество товара в диапазоне от **1** до **10** (метод _**create**_ ресурса **SHOP**).

Выполнить запрос _**search**_. Для полученного ответа сервера написать следующие автотесты:

- Количество товара, полученного по запросу _**search**_, соответствует количеству созданного в _**Pre-request Script**_'е товара.
- **id** полученных по запросу _**search**_ товаров соответствуют **id** созданных в _**Pre-request Script**_'е товаров.
    

По окончании проверки необходимо **удалить** все созданные ранее в _**Pre-request Script**_'е товары.

##### Примечание:

Запросы

- **ДЗ 40-1 SHOP SELECT items из БД Для проверки**
- **ДЗ 40-2 SHOP DELETE Item Для проверки**
    

вспомогательные и служат для ручного отбора и удаления товара в процессе отладки основного запроса.

##### Запрос задания:

- **POST ДЗ 40 SHOP search Поиск товаров**
    

##### Примечание:

1. Запросы к ресурсу **JIRA** требуют авторизации. Параметры авторизации хранятся и заполняются в глобальных переменных _**ATL_USERNAME**_ и _**ALT_PSW**_, метод авторизации в запросах - **Basic Auth**.
2. Запросы к ресурсу **DADATA** требуют авторизации. Параметры авторизации хранятся и заполняются в глобальных переменных **DADATA_AUTH_KEY** и **DADATA_AUTH_VALUE**, метод авторизации в запросах - **API Key**.