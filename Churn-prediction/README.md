# Прогнозирование оттока клиентов банка
<h1>Содержание<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Прогнозирование-оттока-клиентов-банка" data-toc-modified-id="Прогнозирование-оттока-клиентов-банка-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Прогнозирование оттока клиентов банка</a></span><ul class="toc-item"><li><span><a href="#Описание-проекта" data-toc-modified-id="Описание-проекта-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Описание проекта</a></span></li><li><span><a href="#Описание-данных" data-toc-modified-id="Описание-данных-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Описание данных</a></span></li><li><span><a href="#Вывод" data-toc-modified-id="Вывод-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Вывод</a></span></li></ul></li></ul></div>


Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling
## Описание проекта
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Мне предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
## Описание данных
- RowNumber — индекс строки в данных
- CustomerId — уникальный идентификатор клиента
- Surname — фамилия
- CreditScore — кредитный рейтинг
- Geography — страна проживания
- Gender — пол
- Age — возраст
- Tenure — количество недвижимости у клиента
- Balance — баланс на счёте
- NumOfProducts — количество продуктов банка, используемых клиентом
- HasCrCard — наличие кредитной карты
- IsActiveMember — активность клиента
- EstimatedSalary — предполагаемая зарплата
- Exited — Целевой признак, факт ухода клиента

## Вывод
### С дисбалансом:
<br> DecisionTreeClassifier : ROC 0.82, F1 0.52
<br> RandomForestClassifier : ROC 0.85, F1 0.61
### Сбалансированные выборки
Валидационная выборка:
<br> RandomForestClassifier ROC 0.85 , F1 0.62
<br> DecisionTreeClassifier ROC 0.84, F1 0.62
<br> Обе модели показали хорошие результаты по метрикам на валидной выборке.
### тестовая выборка
<br> RandomForestClassifier ROC 0.50 , F1 0.56
<br> DecisionTreeClassifier ROC 0.51, F1 0.62
<br> Модель DecisionTreeClassifier показала лучший результат по полноте и точности обоих выборках.
