# GraphParser
Приложение для нахождения маршрута между двумя точками
# Конфиг файл
Для настройки приложения используется конфиг. 
По умолчанию конфиг считывается с домашней директории, файл MapParser.properties.
 Для указания своего пути используйте 
переменную окружения MAP_PARSER_CONFIG.
## Параметры конфига
* PATH_TYPE - тип маршрута который вы ищете
    * fastest - быстрейший 
    * shortest - кратчайший
    * optimal - оптимальный (выводит все три маршрута кратчайший,
     быстрейший и оптимальный с блокирующими точками)
* OPTIMAL_COEFFICIENT - коэфицент корректировки оптимального маршрута
* MAP_PATH - путь к osm карте
* SPEED_MAP_PATH - путь к карте скоростей
* BLOCK_POINT_PATH - путь к списку блокирующих точек
* ROUTE_OUT_TYPE - тип вывода маршрута
    * simple - вывод дистанции и времени
    * array - вывод дистанции, времени и точек маршрута в виде массива

# Формат записи блокирующих точек
Блокирующие точки записываются в отдельном файле, путь к нему указывается в конфиге.
Каждую точку разделяет перенос строки. Сначала записывается широта затем 
через пробел долгота  
Пример:  
`12.34 11.434`  
`12.45 11.67`

# Запуск
+ заходим корень проекта
+ mvn package
+ java -cp target/GraphParser-1.0-SNAPSHOT.jar Launcher

Выход из программы q.  
Также можно запустить через скрипт finder.sh, для этого читайте usage