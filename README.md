# Django_voting_app
A voting app using Django 

Install pipenv

pip install pipenv

<img width="811" alt="Screenshot 2023-05-30 at 12 32 15" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/c8c96bd8-22ba-40e6-a6f5-a036de06fd02">


Create Venv

pipenv shell

<img width="793" alt="Screenshot 2023-05-30 at 12 33 14" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/c3c8127c-fa9b-4d1d-9c61-7d91cadf92ab">

Install Django

pipenv install django

<img width="764" alt="Screenshot 2023-05-30 at 12 35 24" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/dd22bc0d-d3f8-4b76-8d38-947836a0f5d6">

Create project

django-admin startproject pollster

<img width="794" alt="Screenshot 2023-05-30 at 12 38 28" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/889971d8-fae1-4b2f-b2bf-4f60c061023e">

cd pollster

Click on the url http://127.0.0.1:8082/ to see Django landing page

python manage.py runserver 

<img width="773" alt="Screenshot 2023-05-30 at 12 45 38" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/a4a27425-3e36-4c2d-8d28-c663dbdface1">


<img width="1280" alt="Screenshot 2023-05-30 at 12 46 01" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/0ae51444-817b-4192-9b64-0094f126e232">

Run initial migrations

python manage.py migrate

<img width="661" alt="Screenshot 2023-05-30 at 12 49 31" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/bc30a61f-2b01-4cae-9fee-c1cf28451499">

Create polls app

python manage.py startapp polls

Create polls migrations

python manage.py makemigrations polls

<img width="680" alt="Screenshot 2023-05-30 at 13 15 42" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/d440fbfe-5500-42a2-b30c-ab0291da3dbe">

Run migrations

python manage.py migrate

<img width="696" alt="Screenshot 2023-05-30 at 13 17 41" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/0163f4c3-16ee-479e-89e0-e28f5da427b3">

Using the shell

python manage.py shell

from polls.models import Question, Choice

from django.utils import timezone

Question.objects.all()

q = Question(question_text="What is your favorite Python Framework?", pub_date=timezone.now())

q.save()

q.id

q.question_text

Question.objects.all()

Question.objects.filter(id=1)

Question.objects.get(pk=1)

q = Question.objects.get(pk=1)

q.choice_set.all()

q.choice_set.create(choice_text='Django', votes=0)

q.choice_set.create(choice_text='Flask', votes=0)

q.choice_set.create(choice_text='Flask', votes=0)

q.choice_set.all()

quit()

<img width="801" alt="Screenshot 2023-05-31 at 10 11 37" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/8e2d60ff-e0d7-408c-96e2-fbb4a38c0edc">

Create admin user

python manage.py createsuperuser

<img width="548" alt="Screenshot 2023-05-31 at 10 14 53" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/2e63e8cd-519a-45ee-9027-f693de00b035">

Create pages app

python manage.py startapp pages


Login to the url /admin

<img width="1250" alt="Screenshot 2023-05-31 at 10 18 40" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/55e07d5e-c5a7-4663-929d-caf4a65cf9ba">

<img width="1279" alt="Screenshot 2023-05-31 at 12 46 13" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/3076ac98-3b17-4396-a80c-098b1b1b6615">


<img width="1268" alt="Screenshot 2023-05-31 at 12 50 18" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/5680d982-2699-4a65-baa0-28a8803a8c7e">


<img width="1265" alt="Screenshot 2023-05-31 at 12 50 27" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/4ce2cba2-8861-4b08-8b11-305abc716de3">
