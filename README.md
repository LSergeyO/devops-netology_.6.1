# devops-netology_.6.1
1. 
- Электронные чеки в json виде - MongoDB (документо-ориентированные СУБД) как раз подходит для управления документами и контентом;  
- Склады и автомобильные дороги для логистической компании - Neo4j (графовые СУБД) для построения оптимальных маршрутов;
- Генеалогические деревья - IMS (иерархические СУБД) с одним родителем, либо  IDS (сетевые СУБД) с двумя родителями;  
- Кэш идентификаторов клиентов с ограниченным временем жизни для движка аутенфикации - Memcached (СУБД вида “ключ-значени") для хранения кэш в оперативной памяти;  
- Отношения клиент-покупка для интернет-магазина - PostgreSQL (реляционные СУБД) для хранения данных в таблицах.

2. Данные записываются на все узлы с задержкой до часа (асинхронная запись) - CA, EL-PC;  
При сетевых сбоях, система может разделиться на 2 раздельных кластера - AP, PA-EL;  
Система может не прислать корректный ответ или сбросить соединение - CP, PA-EC.

3. BASE и ACID не могут сочетаться в одной системе, т.к. они  противопоставляющиеся друг другу (один требует обязательной согласовонности, другой нет);

4. Redis - это СУБД вида “ключ-значение” имеет встроенную систему Pub/Sub. Минусы - сложности при работе с большими объемами данных, в частности объем данных не должен превышать объем свободного ОЗУ сервера, иначе работа замедлится.  
