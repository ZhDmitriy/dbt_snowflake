# dbt_snowflake
Работаем с dbt в облачной реляционной базе данных Snowflake

Для запука необходимо: 
1. Установить `dbt-core`: `pip3 install dbt-core`
2. Установить `dbt-snowflake` для подключения к облачной базе данных: `pip3 install dbt-snowflake`
3. Опрелелить файлы .yml вашего dbt проекта и определить пути к ним, когда начнете отлаживать конфигурации: `dbt debug --project-dir C:\Users\Shhhn\PycharmProjects\dbt_course --profiles-dir C:\Users\Shhhn\.dbt`

Где `C:\Users\Shhhn\PycharmProjects\dbt_course` - папка к .yml вашего проекта, а `C:\Users\Shhhn\.dbt` - папка к profiles.yml вашего проекта.

Пример настройки для базы данных Snowflake можно найти по адресу: https://docs.getdbt.com/docs/core/connect-data-platform/snowflake-setup 

4. Если git не установлен на вашем компьютере и/или не установлен в PyCharm - сделайте это. 
5. После запустите команду `dbt debug` с настройками, как указано в пункте 3. После чего, у вас должен быть следующий результат:  
![image](https://github.com/user-attachments/assets/dcb8bfd6-21f6-4683-9d26-4c8209b676ec)

Если плохо знакомы с dbt: https://docs.google.com/document/d/1U-vwwzviZrHjw5umz0RkAf3y2djZUPSu82lK96L6TpU/edit?usp=sharing 

Возможные проблемы при запуске: 

There are 2 unused configuration paths:
- models.dbt_project.staging

Решение: 
1. Используйте правильную структуру docker-compose для dbt проекта
2. schema.yml вынесите в папку models на уровне папок с моделями:

![image](https://github.com/user-attachments/assets/737c8b91-6fd0-4287-906b-9ab8629b25e5)

При работе со Snowflake, создайте новую базу данных и переопределите profiles.yml под созданную базу данных следущим образом: 
![image](https://github.com/user-attachments/assets/1bcd56a4-6bbe-4ae8-b570-9ab76df7010e)

Запустите команду `dbt-run` или `dbt-compile`, чтобы откомпилировать созданные модели и получите следующий результат в консоли: 
![image](https://github.com/user-attachments/assets/81d11973-0078-4959-ad78-4d19a99b3212)

Посмотрим результат в Snowflake базе данных: 
![image](https://github.com/user-attachments/assets/66fff06a-d27b-4c32-8e52-b412c88314b7)

![image](https://github.com/user-attachments/assets/4a106d58-abe2-4390-b06d-4797ca409770)



