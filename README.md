# Видача решти: Жадібний алгоритм та Динамічне програмування

## Опис задачі

У цьому проєкті розроблено дві функції для касового апарату, що визначають оптимальний спосіб видачі решти покупцеві:
1. `find_coins_greedy(amount)`: Використовує жадібний алгоритм для видачі решти.
2. `find_min_coins_top_down(amount)`: Використовує метод динамічного програмування з мемоїзацією (Top-Down).
3. `find_min_coins_bottom_up(amount)`: Використовує метод динамічного програмування (Bottom-Up).

## Жадібний алгоритм

Жадібний алгоритм обирає найбільший можливий номінал монети, поки сума не буде повністю видана. Переваги та недоліки:

- Часова складність: O(n), де n — кількість номіналів монет.
- Швидкий для великих сум.
- Може не давати оптимальний результат для всіх наборів номіналів.

## Динамічне програмування

### Верхній підхід (Top-Down) з мемоїзацією

Цей підхід розбиває основну задачу на підзадачі та розв'язує їх рекурсивно, зберігаючи результати для запобігання повторному обчисленню. Переваги та недоліки:

- Часова складність: O(amount * n), де amount — сума для видачі решти, n — кількість номіналів монет.
- Просторова складність: O(amount) для зберігання результатів підзадач.
- Переваги: Гнучкість та простота в реалізації, особливо для складних задач.
- Недоліки: Використання додаткової пам'яті для мемоїзації.

### Нижній підхід (Bottom-Up)

Цей підхід починає з найдрібніших підзавдань і поступово нарощує розв'язки, рухаючись до розв'язання основного завдання. Переваги та недоліки:

- Часова складність: O(amount * n), де amount — сума для видачі решти, n — кількість номіналів монет.
- Просторова складність: O(amount) для зберігання результатів підзадач.
- Переваги: Явно зрозуміла структура, ефективне використання пам'яті.
- Недоліки: Менш гнучкий у порівнянні з Top-Down підходом.

## Висновки

Жадібний алгоритм є більш ефективним за часом для великих сум і простих наборів номіналів, але не завжди оптимальний. 
Обидва підходи динамічного програмування гарантують оптимальне рішення, але можуть мати різні переваги та недоліки залежно від конкретних умов задачі.
Для різних ситуацій варто обирати відповідний алгоритм залежно від пріоритету: швидкість або оптимальність рішення.
