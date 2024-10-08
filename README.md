# Проект game-dev
В рамках проекта были решены задачи по исследованию нескольких аспектов мобильноЙ игры.

### Стек:  
Проект выполнен с помощью **Python** (билиотеки: **Pandas, SciPy, Seaborn, Plotly**) в **Jupyter Notebook**.
___
### Задачи проекта: 

1. Написать функцию для подсчета retention.
<details><summary>Описание данных</summary>
  
   **df_reg_data (данные о времени регистрации)**  
   *reg_ts* - время регистрации  
   *uid* - уникальный индефикатор пользователя  
   
   **df_auth_data (данные о времени захода пользователей в игру)**  
   *reg_ts* - время захода в игру  
   *uid* - уникальный индефикатор пользователя
  </details>  
  
  2. На основе имеющихся данных A/B тестирования наборов акционных предложений определить, какой набор можно считать лучшим? На основе каких метрик стоит принять правильное решение? 
<details><summary>Описание данных</summary>
  
   **df_2 (данные А/В теста)**  
   *user_id* - уникальный id пользователя  
   *revenue* - доход с пользователя  
   *testgroup* - параметр, обозначающий к какой группе относится пользователь (где **a** - контрольная группа, **b** - тестовая группа)
  </details>  
  
  3. Предложить метрики для оценки результатов последнего прошедшего тематического события в игре.

___
### Этапы выполнения проекта:
1) Написал функцию для расчета Retention игроков, также добавил визуализацию результатов работы функции в Plotly.
2) Выполнил предобработку данных и предварительный анализ.
3) Посчитал и проанализировал продуктовые метрики (Конверсию, ARPPU, ARPU).
4) Проверил гипотезы, проанализировал результаты А/B-теста с использованием теста Хи-квадрат и Bootstrap'а.
5) Выбрал метрики для оценки результатов последнего прошедшего тематического события игры.
___
### Результаты и выводы:
1) Написана гибкая функция для расчета Retention с визуализацией данных.
2) **ARPU** в тестовой группе статистически значимо **НЕ изменился**.  
**Конверсия в платящего пользователя** в тестовой группе статистически значимо **снизилась**.  
**ARPPU** в тестовой группе статистически значимо **НЕ изменился**.  
**Вывод:** акционный набор предложений для контрольной группы можно считать лучше, т.к. ARPU и ARPPU статистически значимо в двух группах не различаются, а конверсия в платящих пользователей в тестовой группе оказалась меньше, чем в контрольной.
3) Предложены метрики для оценки результатов последнего прошедшего тематического события игры.
