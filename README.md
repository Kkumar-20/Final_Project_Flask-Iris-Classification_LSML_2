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

## On Kubernetes
- You can deploy the model/app on Kubernetes with deployment object.

- You can deploy this model/app on Openshift just using git project url with OpenShift build menu.

### Input mlflow ui:

![image](https://user-images.githubusercontent.com/96828026/167298412-d3d32442-c2c3-43f9-8276-c8ad460cb051.png)



### Predictions:

![image](https://user-images.githubusercontent.com/96828026/167298377-51f47ac7-9b3e-4730-8409-608f89df20f1.png)

