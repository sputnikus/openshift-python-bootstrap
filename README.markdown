# OpenShift bootstrap for Python

## Why

There's no official documentation from Red Hat about how to write your WSGI application for OpenShift. So I decided to create bootstrap script to prepare your application directory (currently Flask only) for deployment.

## Usage

Create your app and virtual enviroment

     rhc-create-app -a <app name>
     cd <bootstrap directory>
     ./bootstrap.py <app directory>/env

If you want to activate virtualenv:
     
     cd <app directory>
     source env/bin/activate

And if you want to test your app locally

     cd <app directory>/wsgi
     ./application
