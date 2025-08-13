# Contract Management System

A comprehensive Django-based web application for managing contracts with role-based access control, approval workflows, and document management.

## 🚀 Features

- **User Management & Authentication**
  - Role-based access control (Admin, HR, Legal, Client, Manager)
  - User registration and approval system
  - Secure login/logout functionality

- **Contract Management**
  - Create, view, and manage contracts
  - Multiple contract types (Employment, Service, Partnership, Vendor, Client)
  - Priority levels (Low, Medium, High, Urgent)
  - File upload support for contract documents
  - Contract status tracking (Draft, Pending Review, Approved, Rejected)

- **Approval Workflow**
  - Multi-level approval system
  - Role-based approval permissions
  - Approval remarks and timestamps
  - Contract expiry date management

- **Dashboard & Analytics**
  - Overview of contract statistics
  - Contract list with filtering
  - User-friendly interface

## 🛠️ Technology Stack

- **Backend**: Django 4.x
- **Database**: SQLite (can be configured for PostgreSQL/MySQL)
- **Frontend**: HTML, CSS, JavaScript
- **Authentication**: Django's built-in authentication system
- **File Handling**: Django's FileField for document uploads

## 📋 Prerequisites

- Python 3.8+
- pip (Python package installer)
- Git

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/contract-management-system.git
   cd contract-management-system
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install django
   ```

4. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Open your browser and go to `http://127.0.0.1:8000/`
   - Login with your superuser credentials

## 👥 User Roles & Permissions

| Role | Permissions |
|------|-------------|
| **Admin** | Full access to all features, user management, contract approval |
| **HR** | Create contracts, view all contracts, basic management |
| **Legal** | Contract review and approval, view all contracts |
| **Manager** | Contract approval, view assigned contracts |
| **Client** | View own contracts, limited access |

## 📁 Project Structure

```
contractManagement/
├── contracts/                 # Main app directory
│   ├── models.py             # Database models
│   ├── views.py              # View functions
│   ├── forms.py              # Form definitions
│   ├── urls.py               # URL routing
│   ├── admin.py              # Admin interface configuration
│   ├── signals.py            # Django signals
│   ├── templates/            # HTML templates
│   │   └── contracts/
│   │       ├── dashboard.html
│   │       ├── login.html
│   │       ├── register.html
│   │       ├── create_contract.html
│   │       ├── contract_list.html
│   │       └── approve_contract.html
│   └── static/               # CSS, JS, and other static files
├── contractManagement/        # Project settings
│   ├── settings.py           # Django settings
│   ├── urls.py               # Main URL configuration
│   └── wsgi.py               # WSGI configuration
├── media/                     # Uploaded files
├── manage.py                  # Django management script
└── README.md                  # This file
```

## 🔧 Configuration

### Database Configuration
The default configuration uses SQLite. To use PostgreSQL or MySQL, update the `DATABASES` setting in `contractManagement/settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### Media Files
Uploaded contract files are stored in the `media/` directory. Ensure this directory is writable by your web server.

## 📖 Usage

### For Administrators
1. Access the admin panel at `/admin/`
2. Manage users and their roles
3. Approve new user registrations
4. Monitor all contracts and approvals

### For HR Users
1. Login with HR credentials
2. Create new contracts using the contract creation form
3. Upload contract documents
4. View all contracts in the system

### For Legal/Manager Users
1. Review pending contracts
2. Approve or reject contracts with remarks
3. Set contract expiry dates
4. Monitor contract status

### For Clients
1. Register and wait for approval
2. View contracts assigned to you
3. Monitor contract status and expiry dates

## 🧪 Testing

Run the test suite:
```bash
python manage.py test
```

## 🚀 Deployment

### Production Settings
1. Set `DEBUG = False` in `settings.py`
2. Configure a production database
3. Set up static file serving
4. Configure your web server (Nginx, Apache)
5. Use a production WSGI server (Gunicorn, uWSGI)

### Environment Variables
Create a `.env` file for sensitive configuration:
```bash
SECRET_KEY=your_secret_key_here
DEBUG=False
DATABASE_URL=your_database_url
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:
- Create an issue in the GitHub repository
- Check the documentation
- Contact the development team

## 🔮 Future Enhancements

- [ ] Email notifications for contract updates
- [ ] Contract templates and automation
- [ ] Advanced reporting and analytics
- [ ] Mobile-responsive design improvements
- [ ] API endpoints for external integrations
- [ ] Multi-language support
- [ ] Advanced search and filtering
- [ ] Contract renewal reminders


**Built with ❤️ using Django**

*Last updated: [13-08-2025]*
