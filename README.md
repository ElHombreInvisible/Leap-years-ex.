# Leap-years-ex.
Тренировочное задание по нахождению високосных годов.
## Описание
На вход подается год, необходимо найти 50 ближайших високосных годов к данному. Ближайшими могут быть и более ранние, и более поздние годы. Если введенный год является високосным - он является элементом выходного списка.
Годы необходимо выводить от самого раннего к самому позднему, по году на строку.
Гарантируется, что на вход будет подано целое число.

## Как определить високосный год
распределение високосных годов:
    год, номер которого кратен 400, — високосный;
    остальные годы, номер которых кратен 100, — невисокосные 
    (например, годы 1700, 1800, 1900, 2100, 2200, 2300);
    остальные годы, номер которых кратен 4, — високосные;
    все остальные годы — невисокосные.
## Требования к коду

Код программы должен быть написан на языке Си стандрата c11, по правилам процедурной парадигмы программирования, повторяющиеся блоки кода необходимо вынести в отдельные функции.
При использовании массивов память для них рекомендуется выделять динамически.

## Настройки компилятора
Компиляция производится с помощью компиляторов gcc или clang,с указанием языка Си стандарта c11, со следующими флагами: 
-Wall -Werror -Wextra -fsanitize=address
Имя исполняемого файла - leap_years.
Рекомендуется использовать утилиту make.

## Подсказки
<details>
<summary><b>Использовать в крайнем случае!</b></summary>

<details><summary><b>О структуре кода и последовательности действий</b></summary>
Задачу необходимо декомпозировать - сначала научиться определять високосный год, затем ближайший високосный к введенному, потом создавать списки, отталикваясь от правил поиска и ближайшего найденного года.
ДИНАМИЧЕСКИЕ МАССИВЫ НЕОБХОДИМО ОСВОБОЖДАТЬ
</details>
<details><summary><b>О краевых случаях</b></summary>
При поиске ближайего года необходимо помнить, что он может быть как "справа", так и "слева" на временной шкале, для поиска подходящего года пригодится нахождение остатка от деления по модулю(https://ru.wikipedia.org/wiki/%D0%94%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5_%D1%81_%D0%BE%D1%81%D1%82%D0%B0%D1%82%D0%BA%D0%BE%D0%BC#%D0%92_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8).
При формировании списка-ответа может случиться так, что год с одного края удален от введенного сильнее, чем год с другого края, необходимо контролировать "расстояние" до високосного года, ближайшего ко введенному. (в качестве примера можно попробовать 1700й год)
</details>

</details>
