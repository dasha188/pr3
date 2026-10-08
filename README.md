# CampusFlow — Регистрация на мероприятие

## Макет
- Viewport: 1440 px
- Контейнер: 1200 px
- Боковые поля: 120 px

## Таблица измерений

Элемент           Макет (px)  Реализация (px)  Отклонение 
Container width   1200          1200            0 
Header height     64             64             0
H1 font-size      32             32             0 
Форма width       900           900             0 
Правая панель     260           260             0
Gap колонок       24             24             0 
Input height      44             44             0 
Button height     44             44             0 

## Причины расхождения и исправления

1. Input расширялся при длинном значении → `min-width: 0`.
2. Заголовок выходил за границы → `overflow-wrap: anywhere` + `clamp()`.
3. Не совпадала высота кнопки и input → единая переменная `height: 44px`.

## Использованные единицы

Единица  Где                     Почему 
px       border, radius, height  точные размеры 
%        width: 100%             относительно родителя 
rem      font-size               масштабируемость 
vw       внутри clamp()          адаптивность 
clamp()  H1 font-size            границы 
min()    container width         адаптивная ширина 

## Тесты переполнения
test-1.png - длинный заголовок
test-2.png - длинное ФИО
test-3.png - длинный URL
