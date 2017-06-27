Install
=========

* Open terminal

* Go to the path you want create the project

* Create a virtual machine

```
virtualenv {{ virtual_machine_name }}
```

* Open the virtual machine

```
source {{ virtual_machine_name }}/bin/activate
```

* Create the project

```
django-admin.py startproject --template=https://github.com/pedrosilva88/djagoTemplate/archive/master.zip --extension=py,rst,html {{ project_name }}
```

* Enter in the Prject folder

```
cd {{ project_name }}
```

* Install the requirements
```
    # If Debug
        pip install -r requirements/local.txt
    # If Prod
        pip install -r requirements.txt
```
