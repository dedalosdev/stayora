# stayora
Stayora is an open-source hotel reservation platform featuring a React web interface, a Python/Django/DjangoRestFramework backend and PostgreSQL database. Designed for learning, personal use, and commercial projects, it provides a flexible foundation for building and customizing online stores.

## Included
- `room`: rooms reservation 

# database settings
psql postgres
postgres=# create role postgres with login password 'yourpassword';
postgres=# alter role postgres with login password 'yourpassword';
ALTER ROLE
postgres=# alter role postgres superuser createdb createrole;
ALTER ROLE
postgres=# create database stayora_db owner postgres;
CREATE DATABASE
postgres=# \l
postgres=# \q

# instalation instructions
git clone https://github.com/dedalosdev/stayora.git

cd stayora
cd backend
cp .env.example .env
Edit the database credentials
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
python3 manage.py makemigrations
python3 manage.py migrate
python manage.py createsuperuser

cd frontend
cp .env.example .env
Edit API URL
npm install

# run application
cd backend
python3 manage.py runserver

cd frontend
npm run dev

# URLs
- `http://127.0.0.1:8000/`: The API's urls
- `http://127.0.0.1:8000/api-auth/`: The user authentication
- `http://127.0.0.1:8000/admin/`: The administration interface


## License

Stayora is an open-source project licensed under the MIT License.

You are free to use, copy, modify, distribute, sublicense, and
commercialize this project for personal, educational, or commercial
purposes, subject to the terms of the MIT License.

See the [LICENSE](./LICENSE) file for the complete license text.