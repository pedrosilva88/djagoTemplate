Install
=========

* Open terminal

* Go to the path you want create the project and create a folder

  ```
  mkdir {{ project_name }} && cd {{ project_name }}
  ```

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
   pip install -r requirements/local.txt
    ```

 Database
 =========

  * Open Postgres shell (You should have PostGres installed)

   ```
   sudo su - postgres
   ```

 * Create Database

   ```
   CREATE DATABASE {{ project_name }};
   ```

 * Create User to manage database

   ```

   CREATE USER {{ username }} WITH PASSWORD '{{ password }}';
   ALTER ROLE {{ username }} SET client_encoding TO 'utf8';
   ALTER ROLE {{ username }} SET default_transaction_isolation TO 'read committed';
   ALTER ROLE {{ username }} SET timezone TO 'UTC';
   \q
   ```
