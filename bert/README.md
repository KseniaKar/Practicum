# Обучение модели классификации комментариев

[ipynb](https://github.com/KseniaKar/Portfolio/blob/main/bert/bert.ipynb)
[HTML](https://github.com/KseniaKar/Portfolio/blob/main/bert/bert.html)

## Описание проекта

Требуется анализировать комментарии пользователей на английском языке и выделять токсичные, чтобы отправить на модерацию.


## Цель: 
Обучить модель классифицировать комментарии на позитивные и негативные. Имеется в распоряжении набор данных с разметкой о токсичности правок. Необходимо построить модель со значением метрики качества F1 не меньше 0.75.

## План

Загрузить и подготовьте данные.
Обучить разные модели.
Сделайть выводы.

## Описание данных

Данные находятся в файле toxic_comments.csv. Столбец text в нём содержит текст комментария, а toxic — целевой признак.



## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- transformers.**BertTokenizer**
- sklearn.linear_model.**LogisticRegression**
- sklearn.model_selection.**GridSearchCV**
- catboost.**CatBoostClassifier**



## Вывод

Была проведена исследовательская работа по обработке текстов и обучению и выбору модели для определения токсичных комментариев. Был взят сэмпл из 1000 выборок из всего датасета и получены признаки с помощью предобученной модели BERT на определение токсичности. Получена метрика F1-score: 0.92 на тестовой выборке с помощью модели линейной регрессии.
