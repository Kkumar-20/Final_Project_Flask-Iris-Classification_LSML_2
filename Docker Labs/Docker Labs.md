{\rtf1\ansi\ansicpg1252\cocoartf2638
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 ###############################################################\
#                          WARNING!!!!                        #\
# This is a sandbox environment. Using personal credentials   #\
# is HIGHLY! discouraged. Any consequences of doing so are    #\
# completely the user's responsibilites.                      #\
#                                                             #\
# The PWD team.                                               #\
###############################################################\
[node1] (local) root@192.168.0.8 ~\
$ git clone https://github.com/Kkumar-20/Final_Project_Flask-Iris-Classification_LSML_2\
Cloning into 'Final_Project_Flask-Iris-Classification_LSML_2'...\
remote: Enumerating objects: 187, done.\
remote: Counting objects: 100% (119/119), done.\
remote: Compressing objects: 100% (68/68), done.\
remote: Total 187 (delta 55), reused 96 (delta 42), pack-reused 68\
Receiving objects: 100% (187/187), 994.67 KiB | 12.13 MiB/s, done.\
Resolving deltas: 100% (73/73), done.\
[node1] (local) root@192.168.0.8 ~\
$ cd flask-iris-classification\
bash: cd: flask-iris-classification: No such file or directory\
[node1] (local) root@192.168.0.8 ~\
$ cd Final_Project_Flask-Iris-Classification_LSML_2\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ docker image build -t my_flask_iris:1.0 .\
Sending build context to Docker daemon  1.718MB\
Step 1/8 : FROM python:3.6-slim\
3.6-slim: Pulling from library/python\
a2abf6c4d29d: Pull complete \
625294dad115: Pull complete \
838e3a5a04bf: Pull complete \
e93b4e59b689: Pull complete \
c4401b8c7f9e: Pull complete \
Digest: sha256:2cfebc27956e6a55f78606864d91fe527696f9e32a724e6f9702b5f9602d0474\
Status: Downloaded newer image for python:3.6-slim\
 ---> c1e40b69532f\
Step 2/8 : COPY requirements.txt requirements.txt\
 ---> 1021b23d8d23\
Step 3/8 : RUN pip install --upgrade pip\
 ---> Running in a4ab59449a18\
Requirement already satisfied: pip in /usr/local/lib/python3.6/site-packages (21.2.4)\
Collecting pip\
  Downloading pip-21.3.1-py3-none-any.whl (1.7 MB)\
Installing collected packages: pip\
  Attempting uninstall: pip\
    Found existing installation: pip 21.2.4\
    Uninstalling pip-21.2.4:\
      Successfully uninstalled pip-21.2.4\
Successfully installed pip-21.3.1\
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv\
Removing intermediate container a4ab59449a18\
 ---> e56ff201d6fb\
Step 4/8 : RUN pip install -r requirements.txt\
 ---> Running in 35296a496841\
Collecting pandas==0.25.2\
  Downloading pandas-0.25.2-cp36-cp36m-manylinux1_x86_64.whl (10.4 MB)\
Collecting scikit-learn==0.21.3\
  Downloading scikit_learn-0.21.3-cp36-cp36m-manylinux1_x86_64.whl (6.7 MB)\
Collecting Flask==1.1.1\
  Downloading Flask-1.1.1-py2.py3-none-any.whl (94 kB)\
Collecting Flask-JWT==0.3.2\
  Downloading Flask-JWT-0.3.2.tar.gz (9.9 kB)\
  Preparing metadata (setup.py): started\
  Preparing metadata (setup.py): finished with status 'done'\
Collecting flask-wtf\
  Downloading Flask_WTF-1.0.1-py3-none-any.whl (12 kB)\
Collecting joblib==0.14.0\
  Downloading joblib-0.14.0-py2.py3-none-any.whl (294 kB)\
Collecting WTForms==2.2.1\
  Downloading WTForms-2.2.1-py2.py3-none-any.whl (166 kB)\
Collecting numpy>=1.13.3\
  Downloading numpy-1.19.5-cp36-cp36m-manylinux2010_x86_64.whl (14.8 MB)\
Collecting pytz>=2017.2\
  Downloading pytz-2022.1-py2.py3-none-any.whl (503 kB)\
Collecting python-dateutil>=2.6.1\
  Downloading python_dateutil-2.8.2-py2.py3-none-any.whl (247 kB)\
Collecting scipy>=0.17.0\
  Downloading scipy-1.5.4-cp36-cp36m-manylinux1_x86_64.whl (25.9 MB)\
Collecting Jinja2>=2.10.1\
  Downloading Jinja2-3.0.3-py3-none-any.whl (133 kB)\
Collecting click>=5.1\
  Downloading click-8.0.4-py3-none-any.whl (97 kB)\
Collecting itsdangerous>=0.24\
  Downloading itsdangerous-2.0.1-py3-none-any.whl (18 kB)\
Collecting Werkzeug>=0.15\
  Downloading Werkzeug-2.0.3-py3-none-any.whl (289 kB)\
Collecting PyJWT<1.5.0,>=1.4.0\
  Downloading PyJWT-1.4.2-py2.py3-none-any.whl (15 kB)\
Collecting importlib-metadata\
  Downloading importlib_metadata-4.8.3-py3-none-any.whl (17 kB)\
Collecting MarkupSafe>=2.0\
  Downloading MarkupSafe-2.0.1-cp36-cp36m-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_12_x86_64.manylinux2010_x86_64.whl (30 kB)\
Collecting six>=1.5\
  Downloading six-1.16.0-py2.py3-none-any.whl (11 kB)\
Collecting dataclasses\
  Downloading dataclasses-0.8-py3-none-any.whl (19 kB)\
Collecting zipp>=0.5\
  Downloading zipp-3.6.0-py3-none-any.whl (5.3 kB)\
Collecting typing-extensions>=3.6.4\
  Downloading typing_extensions-4.1.1-py3-none-any.whl (26 kB)\
Building wheels for collected packages: Flask-JWT\
  Building wheel for Flask-JWT (setup.py): started\
  Building wheel for Flask-JWT (setup.py): finished with status 'done'\
  Created wheel for Flask-JWT: filename=Flask_JWT-0.3.2-py3-none-any.whl size=5682 sha256=bba643e66f87283663a5190a269d4d786604663839bec829c8baa384ff8e559c\
  Stored in directory: /root/.cache/pip/wheels/c8/e1/b4/2795e74c0ca84e98d9c5b3c976a4fd6b8a6acb6c8f8c447f6f\
Successfully built Flask-JWT\
Installing collected packages: zipp, typing-extensions, MarkupSafe, importlib-metadata, dataclasses, Werkzeug, six, numpy, Jinja2, itsdangerous, click, WTForms, scipy, pytz, python-dateutil, PyJWT, joblib, Flask, scikit-learn, pandas, flask-wtf, Flask-JWT\
Successfully installed Flask-1.1.1 Flask-JWT-0.3.2 Jinja2-3.0.3 MarkupSafe-2.0.1 PyJWT-1.4.2 WTForms-2.2.1 Werkzeug-2.0.3 click-8.0.4 dataclasses-0.8 flask-wtf-1.0.1 importlib-metadata-4.8.3 itsdangerous-2.0.1 joblib-0.14.0 numpy-1.19.5 pandas-0.25.2 python-dateutil-2.8.2 pytz-2022.1 scikit-learn-0.21.3 scipy-1.5.4 six-1.16.0 typing-extensions-4.1.1 zipp-3.6.0\
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv\
Removing intermediate container 35296a496841\
 ---> b0d5bc9611ce\
Step 5/8 : COPY . /opt/\
 ---> cf45be7f712c\
Step 6/8 : WORKDIR /opt\
 ---> Running in 4c41f624086c\
Removing intermediate container 4c41f624086c\
 ---> 3d221136568a\
Step 7/8 : EXPOSE 8080\
 ---> Running in 0314d78d74b9\
Removing intermediate container 0314d78d74b9\
 ---> d1bbaf5dbfb0\
Step 8/8 : ENTRYPOINT FLASK_APP=app.py flask run --host=0.0.0.0 --port=8080\
 ---> Running in 6f6b30f2917d\
Removing intermediate container 6f6b30f2917d\
 ---> 863f0856928b\
Successfully built 863f0856928b\
Successfully tagged my_flask_iris:1.0\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ docker run --rm --name flask_iris -p 8080:8080 -d my_flask_iris:1.0\
d9826ea59813dcb3d6e11d5de7f7a16f85aa74d1505285efcd8e9b179f48afc7\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ ###############################################################\
#                          WARNING!!!!                        #\
# This is a sandbox environment. Using personal credentials   #\
# is HIGHLY! discouraged. Any consequences of doing so are    #\
# completely the user's responsibilites.                      #\
#                                                             #\
# The PWD team.                                               #\
###############################################################\
[node1] (local) root@192.168.0.8 ~\
$ git clone https://github.com/Kkumar-20/Final_Project_Flask-Iris-Classification_LSML_2\
Cloning into 'Final_Project_Flask-Iris-Classification_LSML_2'...\
remote: Enumerating objects: 187, done.\
remote: Counting objects: 100% (119/119), done.\
remote: Compressing objects: 100% (68/68), done.\
remote: Total 187 (delta 55), reused 96 (delta 42), pack-reused 68\
Receiving objects: 100% (187/187), 994.67 KiB | 12.13 MiB/s, done.\
Resolving deltas: 100% (73/73), done.\
[node1] (local) root@192.168.0.8 ~\
$ cd flask-iris-classification\
bash: cd: flask-iris-classification: No such file or directory\
[node1] (local) root@192.168.0.8 ~\
$ cd Final_Project_Flask-Iris-Classification_LSML_2\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ docker image build -t my_flask_iris:1.0 .\
Sending build context to Docker daemon  1.718MB\
Step 1/8 : FROM python:3.6-slim\
3.6-slim: Pulling from library/python\
a2abf6c4d29d: Pull complete \
625294dad115: Pull complete \
838e3a5a04bf: Pull complete \
e93b4e59b689: Pull complete \
c4401b8c7f9e: Pull complete \
Digest: sha256:2cfebc27956e6a55f78606864d91fe527696f9e32a724e6f9702b5f9602d0474\
Status: Downloaded newer image for python:3.6-slim\
 ---> c1e40b69532f\
Step 2/8 : COPY requirements.txt requirements.txt\
 ---> 1021b23d8d23\
Step 3/8 : RUN pip install --upgrade pip\
 ---> Running in a4ab59449a18\
Requirement already satisfied: pip in /usr/local/lib/python3.6/site-packages (21.2.4)\
Collecting pip\
  Downloading pip-21.3.1-py3-none-any.whl (1.7 MB)\
Installing collected packages: pip\
  Attempting uninstall: pip\
    Found existing installation: pip 21.2.4\
    Uninstalling pip-21.2.4:\
      Successfully uninstalled pip-21.2.4\
Successfully installed pip-21.3.1\
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv\
Removing intermediate container a4ab59449a18\
 ---> e56ff201d6fb\
Step 4/8 : RUN pip install -r requirements.txt\
 ---> Running in 35296a496841\
Collecting pandas==0.25.2\
  Downloading pandas-0.25.2-cp36-cp36m-manylinux1_x86_64.whl (10.4 MB)\
Collecting scikit-learn==0.21.3\
  Downloading scikit_learn-0.21.3-cp36-cp36m-manylinux1_x86_64.whl (6.7 MB)\
Collecting Flask==1.1.1\
  Downloading Flask-1.1.1-py2.py3-none-any.whl (94 kB)\
Collecting Flask-JWT==0.3.2\
  Downloading Flask-JWT-0.3.2.tar.gz (9.9 kB)\
  Preparing metadata (setup.py): started\
  Preparing metadata (setup.py): finished with status 'done'\
Collecting flask-wtf\
  Downloading Flask_WTF-1.0.1-py3-none-any.whl (12 kB)\
Collecting joblib==0.14.0\
  Downloading joblib-0.14.0-py2.py3-none-any.whl (294 kB)\
Collecting WTForms==2.2.1\
  Downloading WTForms-2.2.1-py2.py3-none-any.whl (166 kB)\
Collecting numpy>=1.13.3\
  Downloading numpy-1.19.5-cp36-cp36m-manylinux2010_x86_64.whl (14.8 MB)\
Collecting pytz>=2017.2\
  Downloading pytz-2022.1-py2.py3-none-any.whl (503 kB)\
Collecting python-dateutil>=2.6.1\
  Downloading python_dateutil-2.8.2-py2.py3-none-any.whl (247 kB)\
Collecting scipy>=0.17.0\
  Downloading scipy-1.5.4-cp36-cp36m-manylinux1_x86_64.whl (25.9 MB)\
Collecting Jinja2>=2.10.1\
  Downloading Jinja2-3.0.3-py3-none-any.whl (133 kB)\
Collecting click>=5.1\
  Downloading click-8.0.4-py3-none-any.whl (97 kB)\
Collecting itsdangerous>=0.24\
  Downloading itsdangerous-2.0.1-py3-none-any.whl (18 kB)\
Collecting Werkzeug>=0.15\
  Downloading Werkzeug-2.0.3-py3-none-any.whl (289 kB)\
Collecting PyJWT<1.5.0,>=1.4.0\
  Downloading PyJWT-1.4.2-py2.py3-none-any.whl (15 kB)\
Collecting importlib-metadata\
  Downloading importlib_metadata-4.8.3-py3-none-any.whl (17 kB)\
Collecting MarkupSafe>=2.0\
  Downloading MarkupSafe-2.0.1-cp36-cp36m-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_12_x86_64.manylinux2010_x86_64.whl (30 kB)\
Collecting six>=1.5\
  Downloading six-1.16.0-py2.py3-none-any.whl (11 kB)\
Collecting dataclasses\
  Downloading dataclasses-0.8-py3-none-any.whl (19 kB)\
Collecting zipp>=0.5\
  Downloading zipp-3.6.0-py3-none-any.whl (5.3 kB)\
Collecting typing-extensions>=3.6.4\
  Downloading typing_extensions-4.1.1-py3-none-any.whl (26 kB)\
Building wheels for collected packages: Flask-JWT\
  Building wheel for Flask-JWT (setup.py): started\
  Building wheel for Flask-JWT (setup.py): finished with status 'done'\
  Created wheel for Flask-JWT: filename=Flask_JWT-0.3.2-py3-none-any.whl size=5682 sha256=bba643e66f87283663a5190a269d4d786604663839bec829c8baa384ff8e559c\
  Stored in directory: /root/.cache/pip/wheels/c8/e1/b4/2795e74c0ca84e98d9c5b3c976a4fd6b8a6acb6c8f8c447f6f\
Successfully built Flask-JWT\
Installing collected packages: zipp, typing-extensions, MarkupSafe, importlib-metadata, dataclasses, Werkzeug, six, numpy, Jinja2, itsdangerous, click, WTForms, scipy, pytz, python-dateutil, PyJWT, joblib, Flask, scikit-learn, pandas, flask-wtf, Flask-JWT\
Successfully installed Flask-1.1.1 Flask-JWT-0.3.2 Jinja2-3.0.3 MarkupSafe-2.0.1 PyJWT-1.4.2 WTForms-2.2.1 Werkzeug-2.0.3 click-8.0.4 dataclasses-0.8 flask-wtf-1.0.1 importlib-metadata-4.8.3 itsdangerous-2.0.1 joblib-0.14.0 numpy-1.19.5 pandas-0.25.2 python-dateutil-2.8.2 pytz-2022.1 scikit-learn-0.21.3 scipy-1.5.4 six-1.16.0 typing-extensions-4.1.1 zipp-3.6.0\
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv\
Removing intermediate container 35296a496841\
 ---> b0d5bc9611ce\
Step 5/8 : COPY . /opt/\
 ---> cf45be7f712c\
Step 6/8 : WORKDIR /opt\
 ---> Running in 4c41f624086c\
Removing intermediate container 4c41f624086c\
 ---> 3d221136568a\
Step 7/8 : EXPOSE 8080\
 ---> Running in 0314d78d74b9\
Removing intermediate container 0314d78d74b9\
 ---> d1bbaf5dbfb0\
Step 8/8 : ENTRYPOINT FLASK_APP=app.py flask run --host=0.0.0.0 --port=8080\
 ---> Running in 6f6b30f2917d\
Removing intermediate container 6f6b30f2917d\
 ---> 863f0856928b\
Successfully built 863f0856928b\
Successfully tagged my_flask_iris:1.0\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ docker run --rm --name flask_iris -p 8080:8080 -d my_flask_iris:1.0\
d9826ea59813dcb3d6e11d5de7f7a16f85aa74d1505285efcd8e9b179f48afc7\
[node1] (local) root@192.168.0.8 ~/Final_Project_Flask-Iris-Classification_LSML_2\
$ }
