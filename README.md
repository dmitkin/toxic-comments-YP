## Описание проекта
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.
Необходимо обучить модель классифицировать комментарии на позитивные и негативные. В распоряжении набор данных с разметкой о токсичности правок.

## Описание данных

- _text_ - содержит текст комментария
- _toxic_ - целевой признак

## Вывод
Для обучения модели мы подготовили признаки на основе оценки важности слов TF-IDF. Также мы отдельно создали выборку для теста лучшей модели, выделив ей 25% данных.

Наилучшей моделью оказалась модель основанная на алгоритме логистической регрессии, со значением метрики F1 = 0.77, что намного превосходит показатель метрики модели случайного леса (F1 = 0.34).

Было рассмотрено две модели: модель линейной регрессии и модель случайного леса. Наилучший результат показала модель линейной регрессии со значением метрики F1 на тестовой выборке равным 0.78.
