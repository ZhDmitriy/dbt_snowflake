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


