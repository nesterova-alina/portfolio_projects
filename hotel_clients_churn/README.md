# Прогнозирование оттока клиентов отеля


## Цель проекта

Разработать модель классификации, которая предсказывает отказ от брони.
Если модель покажет, что бронь будет отменена, то клиенту предлагается внести депозит. Размер депозита — 80% от стоимости номера за одни сутки и затрат на разовую уборку. Деньги будут списаны со счёта клиента, если он всё же отменит бронь.

## Данные

Предоставлены исторические данные о характеристиках и поведении клиентов отеля (гражданство, тип заказчика, наличие детей, количество отменённых заказов и др.)  и параметрах бронирования номеров: дата заезда, тип номера, количество изменений заказа и специальных отметок, факт отмены бронирования.

## Задачи

- предобработка и исследовательский анализ данных
- оценка прибыли отеля без внедрения депозитов
- построение моделей логистической регрессии, решающего дерева и случайного леса с подбором различных сочетаний гиперпараметров; выбор лучшей модели
- оценка прибыли, которую принесёт внедрение модели
- выявление признаков ненадёжного клиента


## Итоги

Были обучены модели решающего дерева, решающего леса и логистической регрессии при разных значениях гиперпараметров. Наилучшее качество на обучающей выборке было получено при обучении модели решающего леса со 156 деревьями с макисмальной глубиной 13. На тестовой выборке были получены следующие результаты:
* F1-score = 0.556, AUC_ROC = 0.771
* Доход за 2017 год с депозитом: 35 543 188
* Выручка, принесённая внедрением системы: 4 173 584
Обнаружены важные факторы, повышающие веротяность отмены бронирования: количество дней до предполагаемой даты заезда, наличие у клиента отменённых бронирований в прошлом
Бюджет, выделенный на разработку системы прогнозирования полностью окупился за тестовый период.

## Инструменты и навыки

*pandas*, * numpy*, *sklearn*, *matplotlib*, *seaborn*, *pandas_profiling*