### Description 
1.    Считайте заданный набор данных из репозитария UCI, включая указанный в индивидуальном задании столбец с метками классов.. 

 

2.    Если среди меток класса имеются пропущенные значения, то удалите записи с пропущенными метками класса. Преобразуйте категориальные признаки в числовые при помощи кодирования меток (label encoding). Если в признаках имеются пропущенные значения, то замените пропущенные значения, используя метод, указанный в индивидуальном задании. Если в признаках пропущенных значений нет, то удалите из набора данных записи, идентифицированные как выбросы при помощи метода кластеризации DBSCAN. 

 

3.    Используя метод снижения размерности данных, указанный в индивидуальном задании, определите и оставьте в наборе данных не более четырех признаков. 

 

4.    Нормализуйте оставшиеся признаки набора данных методом, указанным в индивидуальном задании. 

 

5.    Визуализируйте набор данных в виде точек в трехмерном пространстве, отображая точки разных классов разными цветами. При визуализации набора данных используйте три признака с наиболее высокой оценкой важности. В качестве подписей осей используйте названия признаков. В подписи рисунка укажите название набора данных. Создайте легенду набора данных. 

 

6.    Разбейте набор данных на обучающую и тестовую выборки. Создайте и обучите классификатор на основе деревьев решений с глубиной дерева не более 4, определите долю верных ответов на тестовой выборке и визуализируйте границу принятия решений и построенное дерево решений. При визуализации границы принятия решений используйте два признака с наиболее высокой оценкой важности. 

 

7.    Постройте и обучите дополнительные базовые классификаторы, указанные в индивидуальном задании, затем постройте из классификатора дерева решений и дополнительных классификаторов комбинированный классификатор, указанный в индивидуальном задании. Оцените производительность базовых классификаторов и комбинированного классификатора по показателю, указанному в индивидуальном задании. 

 

8.    Постройте и обучите пару ансамблевых классификаторов, указанных в индивидуальном задании, и сравните их производительность по показателю, указанному в индивидуальном задании. 

 

9.    Постройте границы принятия решений ансамблевых классификаторов с визуализацией точек набора данных разных классов разными цветами. Подпишите оси и рисунок.

### Details:
Ecoli Data Set 

Название файла: ecoli.data 

Ссылка: http://archive.ics.uci.edu/ml/datasets/Ecoli 

Класс: localization site (столбец No 9) 

Метод обработки пропущенных значений – медиана признака 

Метод нормализации признаков – масштабирование на интервал [0, 1] 

Алгоритм снижения размерности данных – отбор на основе важности признаков (ExtraTreesClassifier) 

Дополнительные базовые классификаторы: 

⁃               наивный байесовский классификатор 

⁃               классификатор ближайших соседей (к-во соседей = 7) 

Комбинированный классификатор: VotingClassifier 

Ансамблевые классификаторы: BaggingClassifier, RandomForestClassifier 

Показатель качества модели – коэффициент Жаккара (jaccard) 
