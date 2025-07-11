### Description:
1. При помощи модуля sqlite3 откройте базу данных Instacart в файле instacart.db.
2. Загрузите таблицы departments и products в датафреймы Pandas. При помощи запроса SELECT извлеките из таблицы order_products__train записи, соответствующие указанным в индивидуальном задании дню недели (поле order_dow таблицы orders) и коду департамента (поле department_id таблицы products) и загрузите в датафрейм Pandas. Определите количество строк в полученном датафрейме, количество транзакций (покупок) и определите количество товаров (столбец product_id) в транзакциях датафрейма.
3. Выполните к датафрейму запрос, указанный в индивидуальном задании.
4. Постройте транзакционную базу данных из полученного датафрейма, используя в качестве идентификатора транзакции столбец order_id, а в качестве названий товаров - поле product_name из датафрейма для таблицы products, соответствующее столбцу product_id. Найдите в транзакционной базе данных транзакцию с наибольшим количеством товаров и выведите ее на экран.  
5. Постройте по транзакционной базе данных бинарную базу данных в формате датафрейма пакета mlxtend. По бинарной базе данных определите три наиболее популярных товара и определите количество покупок (транзакций) этих товаров.
6. При помощи указанного в индивидуальном задании метода построения популярных наборов предметов постройте популярный набор предметов с минимальной поддержкой не менее 3, имеющий максимальную длину. При отсутствии таких наборов уменьшите поддержку до 2. В случае нехватки вычислительных ресурсов (слишком долгой работы программы) при построении популярных наборов предметов сокращайте число записей в наборе данных (например, делая выборку половины записей набора).
7. Используя пакет mlxtend или реализацию на Python, постройте набор ассоциативных правил для полученного популярного наборов предметов. Используйте уровень достоверности (confidence), равный 0.65.
8. Для построенного набора ассоциативных правил вычислите показатель (меру) оценки ассоциативных правил, указанную в индивидуальном задании, и определите ассоциативные правила с наилучшим значением показателя оценки.


 ### Details:
- Алгоритм: FPMax 

- День недели (поле order_dow таблицы orders): “4” 

- Код департамента (поле department_id таблицы products): “5” 

- Запрос: Определить час дня, в который было совершено более всего покупок (заказов) 

- Показатель оценки ассоциативных правил: рычаг (leverage) 
