# Django_voting_app
A voting app using Django 

Install pipenv

pip install pipenv

Create Venv

pipenv shell

Install Django

pipenv install django

Create project

django-admin startproject pollster

cd pollster

Run server on http: 127.0.0.1:8000 (ctrl+c to stop)

python manage.py runserver

Run initial migrations

python manage.py migrate

Create polls app

python manage.py startapp polls

Create polls migrations

python manage.py makemigrations polls

Run migrations

python manage.py migrate

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

<img width="1279" alt="Screenshot 2023-05-31 at 12 46 13" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/3076ac98-3b17-4396-a80c-098b1b1b6615">


<img width="1268" alt="Screenshot 2023-05-31 at 12 50 18" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/5680d982-2699-4a65-baa0-28a8803a8c7e">


<img width="1265" alt="Screenshot 2023-05-31 at 12 50 27" src="https://github.com/Mamiololo01/Django_voting_app/assets/67044030/4ce2cba2-8861-4b08-8b11-305abc716de3">
