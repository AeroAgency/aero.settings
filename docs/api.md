# API

`Файл класса: lib/config.php`

Класс содержит методы для удобной работы с кастомными значениями:

* `get($config, $option, $cacheTime = 3600)` — Получение значения опции конфигурации.
 Поддерживает стандартное битриксовое кеширование, реализует паттерн Registry,
  сохраняющий последние полученные значения в память объекта.
* `set($config, $option, $value)` — Сохраняет значение опции конфигурации

Пример использования:

```
use Aeroidea\Settings\Config;

// Получение значения настройки root_domain конфигурации proxy
$conf = Config::get('proxy', 'root_domain');

// Установка значения '/home' настройки root_domain конфигурации proxy
Config::set(proxy', 'root_domain', '/home');

```
