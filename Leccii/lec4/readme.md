Лекция 4 Чтение и запись массива в файл  
Задачи  
  
З 1. В следующем текстовом файле ex6-2-b-mountain-data.txt содержатся данные о вершинах-восьмитысячниках в алфавитном порядке.  
  
Использовать метод NumPy genfromtxt для считывания этих данных в соответствующий структурированный массив для определения следующих фактов: а) самая низкая вершина-восьмитысячник; б) самая северная, восточная, южная и западная вершина; в) самое позднее первое восхождение на вершину; г) первая вершина, на которую было совершено восхождение зимой. Также создать другой структурированный массив, содержащий список вершин с указанием их высоты в футах и даты первого восхождения с упорядочением по возрастанию высоты.  
  
    import numpy as np  
  
    data = np.genfromtxt(fname='ex6-2-b-mountain-data.txt',  
                         dtype=[('name', 'S13'), ('height', 'u8'), ('date1', 'S13'), ('date2', 'S13'), ('coords', 'S24')],  
                         skip_header=11,  
                         delimiter=[13, 9, 10, 12, 24],  
                         skip_footer=1)  
					 
    min_height = 9000  
  
    for i in range(0,13 + 1):  
        if min_height > data[i][1]:  
            min_height = data[i][1]  
  
    print('Minimum height = ' + str(min_height))  
  
    import datetime as dt  
  
    start_date = data[0][2]  
  
    least_ascend = data[0][2]  
  
    for i in range(0,13 + 1):  
        if least_ascend > data[i][2]:  
            least_ascend = data[i][2]  
  
    print('Least ascend = ' + str(least_ascend))  