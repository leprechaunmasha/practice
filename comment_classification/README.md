# Проектная работа "Классификация комментариев"

## Цель реализации проекта
Автоматизировать оценку токсичности комментариев.

## Задачи, решаемые в рамках проекта
1. Тексты векторизировать посредством word2vec.
2. К текстам применить технику feature engineering.
3. Построить модель, которая классифицирует комментарии на позитивные и негативные со значением метрики качества F1 не меньше 0.75.
4. Проанализировать набор данных с разметкой о токсичности правок.

## Описание данных
Данные находятся в файле toxic_comments.csv.
  text - текст комментария, 
  toxic — целевой признак.

## Результат
Построена модель логистической регрессии на предобработанных данных, которая даёт результат метрики F1 = 0.75. Из прочих рассмотренных моделей данная наиболее точно угадавает негативные комментарии.

## Использованные библиотеки
* pandas as pd
* numpy as np
* matplotlib.pyplot as plt
* train_test_split из sklearn.model_selection  
* SnowballStemmer из nltk.stem
* stopwords из nltk.corpus
* nltk
* TfidfVectorizer из sklearn.feature_extraction.text
* re
* LogisticRegression из sklearn.linear_model
* cross_val_score sklearn.model_selection
* f1_score из sklearn.metrics
* confusion_matrix из sklearn.metrics
* shuffle из sklearn.utils
* seaborn
* lightgbm as lgb
* LGBMModel, LGBMRegressor из lightgbm 

## Порядок выполнения проекта
1. Загрузить данные.
2. Подготовить данные:
  * Очистить текст от лишних символов (оставить только буквы и пробелы).
  * Привести слова в текстах к единой форме с помощью стемминга, используя SnowballStemmer из библиотеки NLTK.
  * Избавиться от дисбаланса классов.
3. Обучить разные модели.
4. Сделать выводы.

