Install
=========

#### <i class="icon-folder-open"></i> Abrir terminal

#### <i class="icon-folder-open"></i> Ir para a pasta onde vai criar o projeto

#### <i class="icon-folder-open"></i> Criar uma virtual machine virtualenv {{ virtual_machine_name }}

#### <i class="icon-folder-open"></i> Abrir a virtual machine
    source {{ virtual_machine_name }}/bin/activate

#### <i class="icon-folder-open"></i> Criar um project apartir de um template
django-admin.py startproject --template=https://github.com/twoscoops/django-twoscoops-project/archive/master.zip --extension=py,rst,html {{ project_name }}

#### <i class="icon-folder-open"></i> Entrar dentro do Project
    cd {{ project_name }}

#### <i class="icon-folder-open"></i> Instalar os requirements
    # If Debug
        pip install -r requirements/local.txt
    # If Prod
        pip install -r requirements.txt
