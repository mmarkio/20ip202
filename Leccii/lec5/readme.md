Лекция 5 Многочлены  
  
Вопросы  
  
В 1. Третья производная от функции многочлена P(x) = 3x3 + 2x − 7 равна 18, но почему приведенное ниже вычисление дает результат False?  
  
    Polynomial((-7, 2, 0, 3)).deriv(3) == 18  //Так как Polynomial - это объект, а 18 - это Integer  
    False  
  
В 2. Найти и классифицировать критические точки многочлена  

    p1 = Polynomial([-11,1,1])  
    p2 = Polynomial([-7,1,1])  
    p = p1**2 + p2**2  

    dp = p.deriv()  
    stationary_points = dp.roots()  

    ddp = dp.deriv()  

    minima = stationary_points[ddp(stationary_points) > 0]  
    maxima = stationary_points[ddp(stationary_points) < 0]  

    inflections = stationary_points[np.isclose(ddp(stationary_points),0)]  

    print(np.array((minima, p(minima))).T)  

    print(np.array((maxima, p(maxima))).T)  

    print(np.array((inflections, p(inflections))).T)  