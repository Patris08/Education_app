Education_pp

Education_app is a comprehensive web application developed with Django, offering a robust platform for online learning. This application provides features such as user authentication, course creation, module management, various content types (text, files, images, videos), and now, a real-time chat functionality for enhanced collaboration.
Technologies Used

The application leverages the following technologies:

    Django: The primary web framework for building the application.
    uWSGI: A web server gateway interface for serving Django applications.
    Nginx: A high-performance web server used as a reverse proxy for uWSGI.
    Python: The programming language used for backend development.
    HTML, CSS, JavaScript: Frontend technologies for creating a user-friendly interface.
    Django Channels: Introduces support for handling WebSockets, enabling real-time communication.

Features
User Authentication

    Users can create accounts and log in to access courses, modules, and the new chat feature.
    Each user has a profile that tracks the courses they have created and joined.

Course Management

    Users with accounts can create courses, providing information such as title, subject, and an overview.
    Courses can be browsed and joined by other users.

Module Organization

    Courses are organized into modules, each with a title, description, and order.
    The order of modules within a course can be customized.

Content Types

    Modules can contain various content types, including text, files, images, and videos.
    Content types are implemented using Django's GenericForeignKey, allowing flexibility in content creation.

Real-Time Chat

    The application now includes a real-time chat feature, enabling users to communicate within the platform.
    Chat functionality is implemented using Django Channels for WebSocket support.

Content Rendering

    Each content type has a corresponding template for rendering the content in a user-friendly way.
    For example, the Text content type renders text content using a specific template.

Installation

To run the application locally:

    Clone the repository: git clone <repository_url>
    Install dependencies: pip install -r requirements.txt
    Apply database migrations: python manage.py migrate
    Create a superuser account: python manage.py createsuperuser
    Run the development server: python manage.py runserver

Access the application at http://localhost:8000 and the admin interface at http://localhost:8000/admin to start managing courses, content, and engaging in real-time chat.
Deployment

For production deployment, use a production-ready web server like Nginx in combination with uWSGI. Ensure proper configuration and security measures are in place for a production environment.
