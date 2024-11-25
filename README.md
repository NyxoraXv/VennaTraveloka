
Instructions to Run the TravelokaVenna Application

Prerequisites
Before running the application, ensure you have the following installed on your system:
- Python 3.x (latest stable version recommended)
- Pip (Python package manager)

Setup

1. Install Dependencies:
   Install the required Python packages listed in the requirements.txt file. Run the following command in the terminal or command prompt:

   pip install -r requirements.txt

   If a requirements.txt file is unavailable, you can manually install the dependencies:

   pip install azure-ai-inference==1.0.0b5 azure-core==1.30.0 python-dotenv==1.0.0 Django psycopg2-binary waitress whitenoise cryptography

2. Set Up Environment Variables (Optional):
   If you are using a .env file to store environment variables, ensure it is correctly configured in the root directory of the project. Add any required environment variables in this file, such as database credentials or API keys.

Running the Server

To start the application server, run the following command from the project root directory:

python manage.py runserver

This will start the Django development server. By default, the server will run on http://127.0.0.1:8000/.

Accessing the Application

1. Open your web browser.
2. Navigate to the following URL to access the application:

   http://127.0.0.1:8000/

Additional Notes
- Use a virtual environment to isolate dependencies for this project. To create and activate a virtual environment:
  python -m venv venv
  source venv/bin/activate  # On Linux/macOS
  venv\Scripts\activate     # On Windows

- Make sure all dependencies are up to date as listed in the requirements.txt.
- If using a production environment, replace runserver with waitress-serve for better performance:
  waitress-serve --port=8000 TravelokaVenna.wsgi:application

For further assistance, please refer to the official Django documentation or the project maintainers.
