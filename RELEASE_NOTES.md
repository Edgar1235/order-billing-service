# Release v1.1.0 – Data Coupling & Updated Tariffs

## Added
- Спеціальний базовий тариф доставки 80.0 для міста "Kyiv" (50.0 для "Ivano-Frankivsk", 110.0 для інших міст).
- Явний параметр ставки податку `tax_rate` зі значенням за замовчуванням `0.20` у `process_standard_invoice`.

## Changed
- Коефіцієнт доставки за вагу збільшено з `12.0` до `15.0` за кг.
- Перехід на Data Coupling: передаються лише потрібні дані замість цілого об'єкта та глобального стану.

## Breaking Changes
- Видалено глобальну змінну `GLOBAL_TAX_RATE`.
- Видалено `mode_flag` і функцію `process_invoice`; додано `process_standard_invoice` та `process_tax_exempt_invoice`.
- Змінено параметри `calculate_delivery_cost(city, weight_kg)` замість передачі об'єкта користувача.
