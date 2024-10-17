# Product Catalog API

Описание проекта
Этот проект представляет собой простой веб-сервис на базе ASP.NET Core, который предоставляет RESTful API для управления товарами и категориями товаров. В качестве базы данных используется SQLite. Проект реализован с использованием Entity Framework Core для взаимодействия с базой данных.

## Требования:
Для запуска проекта на локальной машине необходимы следующие инструменты:
- .NET 8 SDK
- SQLite

## Установка:
1. Cклонируйте репозиторий проекта (можно сделать, открыв Visual Studio, или через GitBash):  
   `git clone https://github.com/luuave/ProductAPI.git`
2. Запустить проект `ProductCatalogApp.sln`. Перейдите в директорию проекта и выполните команду для установки всех необходимых пакетов (через Terminal):  
    ```
    cd ProductCatalogApp  
    dotnet restore
    ```  
3. Для использования базы данных SQLite необходимо применить миграции. Выполните следующую команду для создания и применения миграций:  
   ```
   dotnet ef migrations add InitialCreate  
   dotnet ef database update
   ```
   Это создаст файл базы данных productcatalog.db в корневой директории вашего проекта.  
5. Запустите приложение:  
   ```
   dotnet run
   ```
7. После успешного запуска, API будет доступно по адресу: https://localhost:5001 или http://localhost:5000.
8. Тестирование API  
После запуска проекта можно протестировать API с помощью инструментов, таких как Postman.  
   `Swagger UI`  
Проект настроен для использования Swagger, чтобы предоставить документацию API.
Там вы сможете видеть доступные эндпоинты и тестировать API напрямую через Swagger UI.
9. Эндпоинты  
# ProductCategory  
- GET /api/ProductCategory — Получить список всех категорий товаров
- POST /api/ProductCategory — Создать новую категорию товара
- PUT /api/ProductCategory/{id} — Обновить категорию товара
- DELETE /api/ProductCategory/{id} — Удалить категорию товара
# Product  
- GET /api/Product — Получить список всех товаров
- POST /api/Product — Создать новый товар
- PUT /api/Product/{id} — Обновить товар
- DELETE /api/Product/{id} — Удалить товар
