entrar sempre no primeiro nível (meeting_planner)

**Rodar server**
python .\manage.py runserver

**Adicionando novo app**
python manage.py startapp appname
adicionar em settings.py o novo app em INSTALLED_APPS

**Mostrar migrations**
python manage.py showmigrations

**Cria migrations**
python manage.py makemigrations

**Cria sql do migrations**
python manage.py sqlmigrate app number

**Aplicar migrations**
python manage.py migrate

**Entrar no Shell do DB**
python manage.py dbshell

**Criar usuário para admin**
python manage.py createsuperuser

**Retrieving Model Data**
#Get all objects
meetings = Meeting.objects.all()
#Get object count
num_meetings = Meeting.objects.count()
#Get a specift object
meeting = Meeting.objects.get(pk=1)

**Get or 404**
from django.shortcuts import get_object_or_404
from .models import Meeting
def detail(request, id):
    meeting = get_object_or_404(Meeting, pk=id)
