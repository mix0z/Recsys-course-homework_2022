# Тask 2
## Что здесь
В данной папке лежат материалы, необходимые для домашней работы по теме 2 "многорукие бандиты". 
## Описание
В файле **sim_lib.py** лежит функция *simulation* которая производит симуляцию жизненного цикла баннеров(Mortal bandits), на некотором абстрактном траффике. Ей на вход подается *policy* и *n* кол-во итераций.  *Policy* это функция со следующей спецификацией: 
* на вход получает лог исторических наблюдений. Это пандас датафрейм, где каждая строка соответствует статистике по одному баннеру, а индекс датафрейма, это номер этого баннера.
* на выходе выдает индекс в датафрейме отвечающий баннеру, который надо выбрать в текущую итерацию. 

В результате работы *simulation* возвращает кумулятивны regret данного полиси при симуляции за *n* шагов. Пример использования симулятора для *e-greedy* бандита находится в ноутбуке **task2_example.ipynb**.
## Использование
В ноутбуке task2_example.ipynb есть сид и бейзлайн регрет для вашей задачи. Необходимо сделать:
 - Написать свое policy, функцию, которая работает согласно спецификации выше. Важно, чтобы это была не e-greedy, а иная полиси(UCB, Thompson sampling или что-то иное)
 - Прогнать свое полиси через *simulation* при  *n*=200k и фиксированном сиде из task2_example.
 - Желательно затюнить свое policy так, чтобы общий регрет был ниже того, который есть в task2_example.
 - Оформить все как юпитер ноутбук в отдельной ветке, сделать пулл реквест с получившейся веткой.
 - Создать папку в формате фамилия.первая_буква_имени (например, ivanov.s). В ней создать папку hw2.
 - В папке hw2 должен быть результирующий нотбук, названный фамилия_первая_буква_имени.ipynb (например, ivanov_s.ipynb), и необходимые скрипты для решения.