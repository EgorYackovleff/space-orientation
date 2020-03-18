# space-orientation
the calculation of space orientation based on the accelerometer, gyroscope and magnetometer
Задачи, которые решаются:

1.

Даны четыре точки в пространстве, с известными координатами в локальной системе координат O. 
Матрицей перспективной проекции было получено двухмерное их представление, т.е. мы имеем координаты этих точек 
в системе координат камеры (таким двухмерным преобразованием может быть снимок обычной камерой или фотоаппаратом). 

Задача состоит в том, чтобы по известным расстояниям между точками в трехмерном мире и их двухмерными проекциям 
определить матрицу перехода от системы координат с центром в точке с камерой и системой координат О. 


Входные данные – координаты точек в системе координат О и их двухмерная проекция. 
Выходные данные – матрица перехода или 6 степеней свободы (координаты x,y,z, углы Эйлера (кватернион)).


Epnp алгоритм. P3P Perspective Three Pointer.


2.

Другая задача:

Задание заключается в том, чтобы написать алгоритм, который сможет максимально точно из исходных данных 
(данные с акселерометра, магнитометра, гироскопа) получить выходной кватернион. 

Все данные в прикрепленном файле, формат записи там же.
С акселерометра поступают проекции ускорений на три оси (нас интересует ускорение свободного падения), 
магнитометр - проекции вектора магнитного поля Земли, гироскоп - угловая скорость датчика. 

Выходной кватернион отражает ориентацию устройства из трех датчиков в пространстве.
