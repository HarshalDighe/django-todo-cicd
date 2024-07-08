# django-cicd -jenkins
A simple todo app built with django

### Setup

Launch Any instance and create file and clone Projects
```
$ mkdir Projects
$ cd Projects
$ git clone https://github.com/shreys7/django-todo.git
```
go to your project 

```bash
$ cd django-todo
```
Downlode the django 

```bash
$ pip install django
```
Once you have downloaded django, run the following command

```bash
$ python3 manage.py makemigrations
```
This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python3 manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python3 manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python3 manage.py runserver 0.0.0.0:8000
```
Once the server is hosted, head over to http://0.0.0.0:8000/todos for the App.

Set the secuirty group and add rule
   - Go to secuirty
   - Edit inbound rule
   - Add rule (Type:Custom TCP, Port Range:8000,Source:Anywhere 0.0.0.0) 

If you get this error

![Screenshot 2024-07-08 175748](https://github.com/HarshalDighe/Spotify-clone/assets/131588514/4c267e87-ffd8-4c14-b433-2cb2c31524ff)

Go to setting.py file
```
vi todoApp/settings.py
```
Search ALLOWED_HOSTS
 
     In allowed hosts add Astricks in single quote. ('*')
     and run server again. 


![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)