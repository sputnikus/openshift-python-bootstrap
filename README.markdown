# OpenShift bootstrap for Python

## Why

There's no official documentation from Red Hat about how to write your WSGI application for [OpenShift](https://openshift.redhat.com/app/express "OpenShift Express"). So I decided to create bootstrap script to prepare your repository for deployment of your [Django](https://www.djangoproject.com/ "Django web framework") or [Flask](http://flask.pocoo.org/ "Flask microframework") application.

## Usage

Create your app and virtual enviroment

     rhc-create-app -a <app name>
     cd <bootstrap directory>
     ./bootstrap.py -f <framework> -n <app name> <app directory>/env

If you want to activate virtualenv:
     
     cd <app directory>
     source env/bin/activate

And if you want to test your app locally

**Flask**:
     
     cd <app directory>/wsgi
     ./application

**Django**:

     cd <app directory>/libs/<app name>
     python manage.py runserver<center></center><center></center> 

## Thanks

* [Ian Weller](http://blog.ianweller.org/2011/05/12/openshift-express-first-thoughts/ "Django in OpenShift")
* [holly's wiki](http://wiki.livedoor.jp/kurt0027/lite/d/openshift%A4%CD%A4%BF "Flask in OpenShift")
* [The virtualenv developers](https://github.com/pypa/virtualenv "Python virtualenv")
