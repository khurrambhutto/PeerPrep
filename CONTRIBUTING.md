# 🤝 Contributing to PeerPrep

Thank you for your interest in contributing to PeerPrep! We welcome contributions from everyone, whether you're fixing bugs, adding new features, improving documentation, or helping with translations.

## 📋 Table of Contents
- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [How to Contribute](#how-to-contribute)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Issue Guidelines](#issue-guidelines)
- [Community](#community)

## 📜 Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. Please treat everyone with respect and create a welcoming environment for all contributors.

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- Git
- Basic knowledge of Django framework
- Virtual environment tool (venv, virtualenv, or conda)

### Development Setup

1. **Fork the repository**
   ```bash
   # Click the "Fork" button on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/your-username/peerprep.git
   cd peerprep
   ```

3. **Set up virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Set up the database**
   ```bash
   python manage.py migrate
   python manage.py createsuperuser  # Optional: create admin user
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Open your browser and go to `http://127.0.0.1:8000/`

## 🛠️ How to Contribute

### Types of Contributions

- **🐛 Bug Reports**: Help us identify and fix issues
- **💡 Feature Requests**: Suggest new features or improvements
- **📝 Documentation**: Improve README, add tutorials, or API docs
- **🧪 Testing**: Write tests or improve test coverage
- **🎨 UI/UX**: Enhance the user interface and experience
- **🔧 Code**: Fix bugs or implement new features

### Finding Issues to Work On

- Look for issues labeled `good first issue` for beginners
- Check issues labeled `help wanted` for general contributions
- Browse the [Issues](https://github.com/your-username/peerprep/issues) page

## 📤 Pull Request Process

1. **Create a new branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b bugfix/issue-description
   ```

2. **Make your changes**
   - Write clean, readable code
   - Follow the coding standards below
   - Add tests for new functionality
   - Update documentation as needed

3. **Test your changes**
   ```bash
   python manage.py test
   python manage.py runserver  # Manual testing
   ```

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add user authentication system"
   ```

5. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request**
   - Go to the original repository on GitHub
   - Click "New Pull Request"
   - Provide a clear title and description
   - Reference any related issues

### Commit Message Guidelines

Use conventional commit format:
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation changes
- `style:` for formatting changes
- `refactor:` for code refactoring
- `test:` for adding tests
- `chore:` for maintenance tasks

Example: `feat: add question voting system`

## 📏 Coding Standards

### Python/Django Standards
- Follow [PEP 8](https://pep8.org/) style guide
- Use meaningful variable and function names
- Write docstrings for functions and classes
- Keep functions small and focused
- Use Django's built-in features when possible

### Frontend Standards
- Write semantic HTML
- Use consistent CSS naming conventions
- Ensure responsive design
- Optimize for accessibility
- Test across different browsers

### File Organization
```
peerprep/
├── models.py          # Database models
├── views.py           # View functions/classes
├── urls.py            # URL patterns
├── forms.py           # Django forms
├── admin.py           # Admin interface
├── tests.py           # Test cases
└── static/            # CSS, JS, images
    ├── css/
    ├── js/
    └── images/
```

## 🧪 Testing

### Running Tests
```bash
# Run all tests
python manage.py test

# Run specific app tests
python manage.py test myapp

# Run with coverage
coverage run --source='.' manage.py test
coverage report
```

### Writing Tests
- Write tests for all new features
- Include edge cases and error conditions
- Use Django's TestCase class
- Mock external dependencies
- Aim for high test coverage

Example test:
```python
from django.test import TestCase
from django.contrib.auth.models import User

class UserTestCase(TestCase):
    def setUp(self):
        self.user = User.objects.create_user(
            username='testuser',
            email='test@example.com',
            password='testpass123'
        )
    
    def test_user_creation(self):
        self.assertEqual(self.user.username, 'testuser')
        self.assertTrue(self.user.check_password('testpass123'))
```

## 🐛 Issue Guidelines

### Reporting Bugs
When reporting bugs, please include:
- **Description**: Clear description of the issue
- **Steps to Reproduce**: Detailed steps to recreate the bug
- **Expected Behavior**: What should happen
- **Actual Behavior**: What actually happens
- **Environment**: OS, Python version, browser (if applicable)
- **Screenshots**: If applicable

### Feature Requests
For feature requests, please include:
- **Problem**: What problem does this solve?
- **Solution**: Describe your proposed solution
- **Alternatives**: Any alternative solutions considered
- **Additional Context**: Screenshots, mockups, or examples

## 🌟 Recognition

Contributors will be recognized in:
- README.md contributor list
- Release notes for significant contributions
- Special mentions in project updates

## 💬 Community

### Getting Help
- **GitHub Issues**: For bug reports and feature requests
- **Discussions**: For general questions and community chat
- **Email**: [maintainer@peerprep.com] for private matters

### Communication Guidelines
- Be respectful and inclusive
- Use clear, concise language
- Provide context and examples
- Search existing issues before creating new ones

## 📚 Additional Resources

- [Django Documentation](https://docs.djangoproject.com/)
- [Python Style Guide](https://pep8.org/)
- [Git Workflow](https://guides.github.com/introduction/flow/)
- [Markdown Guide](https://www.markdownguide.org/)

---

**Happy Contributing! 🎉**

Your contributions help make PeerPrep a better platform for student learning and collaboration. Thank you for being part of our community!