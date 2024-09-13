# Django Commands

This guide outlines various Django commands.

## Remember:
- Windows use **py**
- MacOS, python3

## Commands:

- **Start the development server**
    ```
    python3 manage.py runserver
    ```

- **Make migrations (assuming you have models.py with model definitions)**
    ```
    python3 manage.py makemigrations
    ```

- **Apply migrations to the database**
    ```
    python3 manage.py migrate
    ```

- **Collect static files (assuming you have static files in your project)**
    ```
    python3 manage.py collectstatic
    ```

- **Create a superuser account (replace 'username' and 'password' with your desired credentials)**
    ```
    python3 manage.py createsuperuser username password
    ```

- **Start a python3 shell with the Django environment loaded**
    ```
    python3 manage.py shell
    ```

- **Check for project issues (replace '--all' with specific checks if desired)**
    ```
    python3 manage.py check
    ```

- **Load fixture data into the database (assuming you have a fixture file named 'mydata.json')**
    ```
    python3 manage.py loaddata mydata.json
    ```

- **Dump the database contents to a fixture file (replace 'mydata.json' with your desired filename)**
    ```
    python3 manage.py dumpdata > mydata.json
    ```