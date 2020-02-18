# Task_1_2_3

## Task 1: Iris.ipynb 

Przedstawiłem kilka modeli bibloteki scikit-learn 
Wcześniej konieczne było wstępne obrobienie danych: 
Tj. 
Replace , to . in Petal.Width and change object to float64
data['Petal.Width'] = data['Petal.Width'].str.replace(',','.').astype(np.float64)

There is a data where length is < 0 - remove or reaplace 
Convert to absolute value
data['Sepal.Length'] = data['Sepal.Length'].abs()

Drop nan records if exists
data = data.dropna()

## Task 2: Headlines.ipynb 

Skorzystałem uczenia głębokiego z wykorzystaniem silnika tensorflow - w mojej konfiguracji korzystający z CPU
Trenowanie odbyło się na 25 epokach, chociaż zakładam, że zbliżony wynik można byłoby osiągnąć na 15-stu

## Task 3:

SELECT * FROM students WHERE student_id IN (
SELECT  student_id FROM exam_results AS e_r
INNER JOIN class_catalogue as c_c ON c_c .class_id = e_r. class_id
WHERE c_c.class_name = ’algebra‘ AND grade >= 4 )
