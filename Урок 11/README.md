## **Коллекция ДЗ Урок 11.** Валидация ответа по JSON Schema

#### Задание 49.

**JIRA**, метод _**getIssue**_. Обратиться к задаче _**TV-4**_ и сверить полученный от сервера ответ со схемой. Для проверки схемы использовать библиотеку _**tv4**_. На случай падения валидации схемы предусмотреть вывод в консоль информации о конкретном месте несовпадения.

##### Запрос задания:

- **GET ДЗ 49 JIRA getIssue Тестируем схему ответа с помощью tv4**
    

#### Задание 50.

**JIRA**, метод _**getIssue**_. Обратиться к задаче _**TV-4**_ и сверить полученный от сервера ответ со схемой. Для проверки схемы использовать библиотеку _**ajv**_. На случай падения валидации схемы предусмотреть вывод в консоль информации о конкретном месте несовпадения.

##### Запрос задания:

- **GET ДЗ 50 JIRA getIssue Тестируем схему ответа с помощью ajv**
    

#### Задание 51.

**SHOP**, метод _**create**_. Для указанного метода написать схему валидации ответа. Выполнить запрос, сверить полученный от сервера результат с написанной схемой. Для проверки можно использовать любую из двух применявшихся ранее библиотек. На случай падения валидации схемы предусмотреть вывод в консоль информации о конкретном месте несовпадения.

##### Примечание:

Запросы

- **ДЗ 51-1 SHOP SELECT items из БД Для проверки**
- **ДЗ 51-2 SHOP DELETE Item Для проверки**
    

вспомогательные, служат для отбора и удаления оставшегося после основного запроса "мусора".

##### Запрос задания:

- **POST ДЗ 51 SHOP create Создать товар Проверить схему**
    

#### Задание 52.

**DADATA**, поиск по фамилии. Для указанного метода написать схему валидации ответа. Отправить ресурсу **DADATA** запрос, тело которого имеет вид:

``` json
{
  "query": "Ан"
}

 ```

Сверить полученный от сервера результат с написанной схемой. Для проверки можно использовать любую из двух применявшихся ранее библиотек. На случай падения валидации схемы предусмотреть вывод в консоль информации о конкретном месте несовпадения.

##### Запрос задания:

- **POST ДЗ 52 DADATA Поиск по фамилии Проверить схему**
    

##### Примечание:

1. Согласно рекомендациям разработчиков **Postman**, предпочтительнее использовать библиотеку _**ajv**_ для проверок схемы, _**tv4**_ устарела.
2. Для "черновой" генерации схемы целесообразно использовать один из генераторов схемы по **JSON** (например, [JSONschema.net](https://jsonschema.net)): полученный от сервера ответ помещаем в генератор, получаем схему, просматриваем ее и правим под свою задачу.
3. Запросы к ресурсу **JIRA** требуют авторизации. Параметры авторизации хранятся и заполняются в глобальных переменных _**ATL_USERNAME**_ и _**ALT_PSW**_, метод авторизации в запросах - **Basic Auth**.
4. Запросы к ресурсу **DADATA** требуют авторизации. Параметры авторизации хранятся и заполняются в глобальных переменных **DADATA_AUTH_KEY** и **DADATA_AUTH_VALUE**, метод авторизации в запросах - **API Key**.