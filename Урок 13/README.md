## **Коллекция ДЗ Урок 13.** Организация тестов. SQL через Postman

#### Задание 55.

**SHOP**. Методом _**create**_ создать новый товар, включая его изображение. Методом **uploadPhoto** загрузить дополнительное изображение созданного ранее товара. Написать автотесты, проверяющие создание нового товара, включая формат изображения (_**base64**_), успешную загрузку дополнительного изображения товара, а также автотесты, проверяющие внесение информации об изображениях созданного ранее товара в БД магазина.

##### Запросы задания:

- **POST ДЗ 55-1 SHOP create Создать товар с фото**
- **POST ДЗ 55-2 SHOP uploadPhoto Загрузить дополнительное фото к созданному товару**
- **POST ДЗ 55-3 SHOP select SQL over API Выборка фото созданного товара**
- **POST ДЗ 55-4 SHOP delete Удаление созданного товара**
    

##### Примечание:

1. Для передачи id созданного товара ао цепочке запросов служит переменная коллекции productId, не требующая ручного заполнения.
2. Запрос **POST ДЗ 55-4 SHOP delete Удаление созданного товара** вспомогательный, служит для удаления тестовых данных из БД магазина.