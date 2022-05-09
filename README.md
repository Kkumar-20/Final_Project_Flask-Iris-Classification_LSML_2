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

