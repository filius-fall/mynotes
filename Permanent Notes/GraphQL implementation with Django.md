
I have stumbled upon GraphQL at my work and found it very fascinating and wanted to build some projects inorder to learn it and also to revise my knowledge in those respective framework

This Blog is about implementation in Django Framework


First create a virtual environment

``` Bash TI:"Virtual env installation" HL:"1" FOLD
$ python3 -m venv <name-of-your-env>
```

I am using venv to create my virtualenv, you can use any virtualenv of your choice like conda or virtualenv

and activate your virtualenv

```Shell
$ source <env-name>/bin/activate
```

Now pip install following pacakges

``` SHELL
$ pip install django graphene-django
```

Now start django project and graphql app using the following commands

```Shell
$ django-admin startproject graph_katas
$ django-admin startapp book_project
```

I am doing this project to practice the Graphql implementation with Django so thats why i named it graph_katas since 