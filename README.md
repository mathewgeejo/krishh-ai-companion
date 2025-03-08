# Krishh  

## Overview  

Krishh is an AI-powered educational assistant designed to help students learn in an interactive and informative way. It provides structured answers to any question, ensuring responses are tailored for educational purposes. Whether it's science, math, history, or any subject, Krishh delivers clear and insightful explanations to support learning.  

Krishh is optimized to run on a Raspberry Pi, making it accessible for students, educators, and DIY tech enthusiasts. Additionally, it can be deployed on a humanoid automaton, bringing a more engaging and interactive learning experience to life.  

## Features  

- AI-driven, student-friendly responses  
- Runs efficiently on Raspberry Pi  
- Supports deployment on humanoid robots  
- Covers a wide range of academic subjects  
- Interactive and voice-enabled (if applicable)  

## Prerequisites  

Before setting up Krishh, ensure you have the following installed:  

- Operating System: Raspberry Pi OS, Linux, or Windows  
- Python: Version 3.8 or higher  
- Git: For cloning the repository  
- Any other dependencies as required  

## Installation  

Follow these steps to set up the project locally:  

1. Clone the repository  

   Open your terminal and run:  

   ```bash
   git clone https://github.com/mishalshanavas/Krish-v2.git
   ```

   Navigate to the project directory:  

   ```bash
   cd Krish-v2
   ```

2. Set up a virtual environment (recommended)  

   It's advisable to use a virtual environment to manage dependencies:  

   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows, use 'env\Scripts\activate'
   ```

3. Install dependencies  

   Ensure pip is up to date:  

   ```bash
   pip install --upgrade pip
   ```

   Install the required packages:  

   ```bash
   pip install -r requirements.txt
   ```

4. Configure environment variables  

   Create a `.env` file in the root directory and add necessary environment variables:  

   ```env
   SECRET_KEY=your_secret_key
   DEBUG=True
   DATABASE_URL=your_database_url
   ```

   Replace placeholders with actual values.  

5. Apply database migrations  

   Set up the database schema:  

   ```bash
   python manage.py migrate
   ```

6. Create a superuser (optional)  

   For admin access:  

   ```bash
   python manage.py createsuperuser
   ```

   Follow the prompts to set up credentials.  

## Running the application  

To start the development server:  

```bash
python manage.py runserver
```

Access the application at `http://127.0.0.1:8000/`.  

## Running tests  

Ensure code quality and functionality by running tests:  

```bash
python manage.py test
```

## Deployment  

For deploying Krishh to a production environment:  

1. Set `DEBUG=False` in your `.env` file.  
2. Configure allowed hosts:  

   ```env
   ALLOWED_HOSTS=your_domain.com
   ```  

3. Set up a production-ready web server  

   Use servers like Gunicorn combined with Nginx for deployment.  

4. Secure the application  

   - Use HTTPS  
   - Regularly update dependencies  
   - Monitor logs for any anomalies  

## Contributing  

We welcome contributions! To get started:  

1. Fork the repository.  
2. Create a new branch:  

   ```bash
   git checkout -b feature/your_feature_name
   ```  

3. Commit your changes:  

   ```bash
   git commit -m "Add your message"
   ```  

4. Push to the branch:  

   ```bash
   git push origin feature/your_feature_name
   ```  

5. Open a pull request.  

Please ensure your code adheres to our coding standards and includes relevant tests.  

## License  

This project is licensed under the [MIT License](LICENSE).  
