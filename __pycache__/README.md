### Start virtual environment
```source env/bin/activate```

### Freeze installed modules
- Run evertime you install a new module to keep up to date
```pip freeze > requirements.txt```

### Source .env file
```source .env```

### Start flask server
```flask run```

### Migrate changes to postgress database
```python manage.py db migrate```
```python manage.py db upgrade```

### Adding test user to test SQLAlchemy connection
```python```
```from app import db```
```from app.models import User```
```u = User(username='new_user', email='new@email.com')```
```u.set_password('password')```
```exit()```

### Verify successful add new user
```python```
```from app import db```
```from app.models import User```
```users = User.query.all()```
```for user in users:print(user.username)```
```for user in users: print(user.password_hash)```


