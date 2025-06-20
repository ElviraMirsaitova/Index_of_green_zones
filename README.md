Описание задания:
Вы работаете в аналитическом отделе экологической службы города. Ваша задача — написать функцию, которая будет рассчитывать индекс озеленения для различных территорий. Индекс озеленения определяется как отношение общей площади зелёных зон к общей площади территории.

Однако данные, которые вы получаете, не всегда идеальны. В данных о зелёных зонах могут отсутствовать значения. Это происходит из-за того, что некоторые участки ещё не были полностью исследованы или их данные временно недоступны. Вам нужно учесть это при расчёте индекса озеленения.

Условие задачи:
Вам дан список словарей, описывающий территории. Каждый такой словарь содержит следующие ключи:

"territory_name" — название территории;
"territory_area" — общая площадь территории;
"green_zones" — список площадей зелёных зон.
Гарантируется, что названия территорий не повторяются и площадь территории положительное число.
А вот список площадей зелёных зон может содержать как положительные числа и так и значения None.

Необходимо написать функцию calculate_green_index, которая:

Принимает список словарей территорий.
Возвращает новый словарь, где:
Ключом является название территории.
Значением является индекс озеленения округлённый до трёх знаков после запятой.
Индекс озеленения рассчитывается по формуле:

Индекс озеленения
=
Сумма площадей зелёных зон
Общая площадь территории

Если в списке площадей зелёных зон встречаются значения None, они должны быть проигнорированы при подсчёте суммы площадей зелёных зон.

Пример входных данных:
[
    {
        "territory_name": "Пушкин",
        "territory_area": 89.24,
        "green_zones": [15.7344, 9.44, None, 2.49]
    },
    {
        "territory_name": "Павловск",
        "territory_area": 36.8,
        "green_zones": [3.82, 2.865, 1.91]
    },
    {
        "territory_name": "Петергоф",
        "territory_area": 48.3,
        "green_zones": [4.5, 9, 2.25]
    }
]
Ожидаемый результат:
{
    "Пушкин": 0.31,
    "Павловск": 0.234,
    "Петергоф": 0.326
}
