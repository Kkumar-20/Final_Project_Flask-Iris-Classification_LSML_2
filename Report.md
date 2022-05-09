# Final Project Flask Iris Classification
This is a simple iris flower classification model deployment project as flask app.

## Directly run on Docker without building

`  docker run --rm -d -p 8080:8080 erkansirin78/flask-iris-classification:2021-3 `

## Build an image (Dockerize) and run on Docker container
- Download project
` git clone https://github.com/erkansirin78/flask-iris-classification.git ` 

` cd flask-iris-classification `

- Build image 
` docker image build -t my_flask_iris:1.0 . ` 

- Run container 
` docker run --rm --name flask_iris -p 8080:8080 -d my_flask_iris:1.0 ` 

- Open browser http://localhost:8080/

Enjoy your predictions.
# Mlflow
## mlruns/artifacts
- MLmodel
- conda.yaml
- model.pkl
- requirements.txt

## mlruns/params
- alpha
- l1_ratio

## mlruns/tags/
- mlflow.log-model.history
- mlflow.source.name
- mlflow.source.type
- mlflow.user

# Data Set Description

1. Predicted attribute: class of iris plant.
2. This is an exceedingly simple domain.
3. Number of Instances: 150 (50 in each of three classes)

4. Number of Attributes: 4 numeric, predictive attributes and the class

5. Attribute Information:
   1. sepal length in cm
   2. sepal width in cm
   3. petal length in cm
   4. petal width in cm
   5. class: 
      -- Iris Setosa
      -- Iris Versicolour
      -- Iris Virginica

6. Missing Attribute Values: None

7. Summary Statistics:
	         Min  Max   Mean    SD   Class Correlation
   sepal length: 4.3  7.9   5.84  0.83    0.7826   
    sepal width: 2.0  4.4   3.05  0.43   -0.4194
   petal length: 1.0  6.9   3.76  1.76    0.9490  (high!)
    petal width: 0.1  2.5   1.20  0.76    0.9565  (high!)

8. Class Distribution: 33.3% for each of 3 classes.

## On Kubernetes
- You can deploy the model/app on Kubernetes with deployment object.

- You can deploy this model/app on Openshift just using git project url with OpenShift build menu.

### Input mlflow ui:

![image](https://user-images.githubusercontent.com/96828026/167298412-d3d32442-c2c3-43f9-8276-c8ad460cb051.png)



### Predictions:

![image](https://user-images.githubusercontent.com/96828026/167298377-51f47ac7-9b3e-4730-8409-608f89df20f1.png)

### Step-by-step process of deploying a model to production
- Elasticnet model (alpha=0.300000, l1_ratio=0.500000):
  - RMSE: 0.22744552699068046
  - MAE: 0.2016874375196894
  - R2: 0.7887631733620541
- Elasticnet model (alpha=0.300000, l1_ratio=0.300000):
  - RMSE: 0.21430541884512883
  - MAE: 0.19068179306295002
  - R2: 0.8124655154355901
- Elasticnet model (alpha=0.800000, l1_ratio=0.500000):
  - RMSE: 0.3388654849846033
  - MAE: 0.3143659462145404
  - R2: 0.5311115809351108
- Elasticnet model (alpha=0.450000, l1_ratio=0.300000):
  - RMSE: 0.23220806152760973
  - MAE: 0.20570007884891398
  - R2: 0.7798242826598251
- Elasticnet model (alpha=0.200000, l1_ratio=0.300000):
  - RMSE: 0.20467188959740729
  - MAE: 0.18074904196419297
  - R2: 0.8289467885685591
- Elasticnet model (alpha=0.900000, l1_ratio=0.900000):
  - RMSE: 0.5063373885270652
  - MAE: 0.47448979591836743
  - R2: -0.046875
  
### Asynchronous Iris Project
Task 03c90830-40f0-42e7-8882-bfe7a4ceeeb5
Status - DONE
{'setosa': 50}

### MLflow_Architecture
```
Predictions: <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Prediction</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
   
</head>
<body>
<div class="container">
    <div class="row">
        <div class="span4"></div>
        <div class="span4">

<h1>FLASK APP RUNNING</h1>
<h2>Please enter your flower measurements below:</h2>
<form method="POST">
    
    <input id="csrf_token" name="csrf_token" type="hidden" value="ImU0ZjE0YjY4NTNjZWI2MDdjZmJhNjFlNDliZmE4ZjAwODdjOGY1YmYi.Ynfryg.dIV-J3kedB-kYBAp1Jz7bV77MTU">
    <table class="table">
        <tr>
        <th>Attribute</th>
        <th>Value</th>
    </tr>
        <tr>
            <td> <label for="SepalLengthCm">Sepal Length</label></td>
            <td> <input id="SepalLengthCm" name="SepalLengthCm" type="text" value=""></td>
        </tr>

    <tr>
        <td><label for="SepalWidthCm">Sepal Width</label></td>
        <td> <input id="SepalWidthCm" name="SepalWidthCm" type="text" value=""></td>
    </tr>

    <tr>
        <td><label for="PetalLengthCm">Petal Length</label></td>
        <td><input id="PetalLengthCm" name="PetalLengthCm" type="text" value=""></td>
    </tr>

    <tr>
        <td><label for="PetalWidthCm">Petal With</label></td>
        <td><input id="PetalWidthCm" name="PetalWidthCm" type="text" value=""></td>
    </tr>
    </table>
    <input id="submit" name="submit" type="submit" value="Predict">
</form>
</div>
<div class="span4"></div>


</div>
</div>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
</body>
</html>
```
### Mean Average Error(mae)
1652027686016 0.2016874375196894 0
### r2
1652027686006 0.7887631733620541 0
### rmse
1652027685996 0.22744552699068046 0
