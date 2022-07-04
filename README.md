[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8082446&assignment_repo_type=AssignmentRepo)
# Boids

Материалы:
- https://en.wikipedia.org/wiki/Boids
- условия задачи: http://www.red3d.com/cwr/boids/
- пример выполнения: https://eater.net/boids

Задачи:
1. Описать предметную область (домен):
    - выделить объекты, их свойства и функции
    - дать определения объектам через другие объекты
2. Описать шаги выполнения программы
    - основные этапы вычислений
    - функции - что делаем внутри этапов
3. Описать ход решения в виде цепочки промежуточных реализаций (программа 1, программа 2, …)
4. Реализовать решение по описанию п. 1-3

Пункты 1 - 3 вставлять текстом под этой чертой:

--------------------
1. Предметная область:
    - Птицы (Boids) - объекты, с такими полями как координаты (по x и y), вектор скорости, радиус видимости, угол обзора (возможно, необходимо будет добавить и другие). Птицы должны обладать функциями поиска птиц в радиусе видимости, а также постороения векторов движения при 3 разных поведениях: Separartion, Alignment и Cohesion.
    - Поле - объект, на котором будут отображаться птицы. Полями поля будут его размеры. У поля должно быть как минимум 2 основных метода: отрисовка поля, обновление поля.
2. Шаги выполнения программы:  
    Инициализировать_поле( )  
    Инициализировать_массив_птиц( )  
    **WHILE**  
    **DO**  
    Отрисовать_поле( )  
    Обновить_поле( ){  
    **FOR** i: все объекты Boids  
    Поиск_птиц_в_области()  
    Вектор1 = Separation()  
    Вектор2 = Alignment()  
    Вектор3 = Cohesion()  
    ВекторПеремещения = Вычислить_вектор(Вектор1, Вектор2, Вектор3)  
    Выполнить_перемещение(ВекторПеремещения)  
    **END FOR**   
    }  
    **END WHILE**
3. Ход решения
    - Создание поля (с использованием OpenGL или другой библиотеки)
    - Создание объекта Boid, проверка изменение его координат во времени
    - Реализация каждого из поведений
    - Реализация перемещения объекта, учитывая сразу все поведения