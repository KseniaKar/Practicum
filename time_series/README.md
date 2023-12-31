# Прогноз количества заказов для сервиса такси

[ipynb](https://github.com/KseniaKar/Portfolio/blob/main/time_series/time%20series.ipynb)
[HTML](https://github.com/KseniaKar/Portfolio/blob/main/time_series/time_series.html)

## Описание проекта

Компания такси собрала исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. **Цель**: построить модель для такого предсказания. Значение метрики RMSE на тестовой выборке должно быть не больше 48.


## План

- Загрузить данные и выполнить их ресемплирование по одному часу.
- Проанализировать данные.
- Обучить разные модели с различными гиперпараметрами. Сделать тестовую выборку размером 10% от исходных данных.
- Проверить данные на тестовой выборке и сделать выводы.

## Описание данных
Данные лежат в файле taxi.csv. Количество заказов находится в столбце num_orders.


## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- statsmodels.tsa.seasonal.**seasonal_decompose**
- sklearn.model_selection.**TimeSeriesSplit**
- sklearn.model_selection.**GridSearchCV**
- sklearn.metrics.**mean_squared_error**
- sklearn.metrics.**make_scorer**
- sklearn.linear_model.**LinearRegression**
- sklearn.ensemble.**RandomForestRegressor**
- catboost.**CatBoostRegressor**
- **matplotlib**



## Вывод

- Проанализирован ряд моделей машинного обучения для предсказания времянного ряда.
- Подобраны гиперпараметры для различных моделей.
- Лучше всего показали себя CatBoost и LightGBM и LinearRegression, у которых почти одинаковый RMSE.
- RMSE LinearRegression на тестовой выборке: 38.93, в сравнении предсказание средним дает 58.66.
- На тестовой выборке CatBoost показал результат лучше RMSE 38.93.



