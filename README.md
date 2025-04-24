# Sentinel Shield

## Overview
Sentinel Shield is a modern passport verification and border control system that streamlines the traditional passport control method. Instead of relying on physical stamps and manual verification, this application enables swift passport verification within seconds, ensuring seamless entry into destination countries while maintaining maximum security.

## Features
- **Passport Verification**: Validates passport authenticity and expiration
- **Visa Verification**: Checks visa validity and requirements
- **Security Checks**: Cross-references with wanted lists for security concerns
- **Health Verification**: Validates health/vaccination requirements for different countries
- **Face Recognition**: Matches passport holders with their identification photos
- **QR Code Scanning**: Fast passport data retrieval via QR codes
- **Admin Dashboard**: Manage users and system access

## Technologies Used
- **Backend**: Flask (Python)
- **Database**: MySQL via XAMPP (locally)
- **Face Recognition**: OpenCV and face_recognition libraries
- **Frontend**: HTML, CSS, JavaScript
- **Authentication**: Custom login system

## Project Structure
- `combine.py`: Main application file containing routes and business logic
- `templates/`: HTML templates for the web interface
- `static/`: CSS, JavaScript, and static assets
- `Faces/`: Directory storing facial recognition data

## Local Development Setup

### Prerequisites
- Python 3.8+
- XAMPP with MySQL
- Git

### Installation Steps
1. Clone the repository
   ```
   git clone <repository-url>
   cd sentinel-shield
   ```

2. Install required Python packages
   ```
   pip install -r requirements.txt
   ```

3. Set up the database
   - Start XAMPP control panel and ensure MySQL is running
   - Create a database named 'sentinel'
   - Import the database schema (not included in repo, contact administrators)

4. Run the application
   ```
   python combine.py
   ```
   The application will be available at http://localhost:5000

## Database Schema
The system utilizes several key tables:
- `passport_holders`: Stores passport information and personal details
- `passengers`: Travel information for passport holders
- `visadetails`: Visa information and validity 
- `wanted_list`: Security database for restricted individuals
- `healthdetails`: Health and vaccination records
- `verified`: Successfully verified travelers
- `officers`: System users with authentication details

## Usage Guide
1. **Login**: Access the system through the login page
2. **QR Scanning**: Scan the QR code on a passport
3. **Face Verification**: The system captures and compares the person's face with the passport photo
4. **Verification Process**: The system checks passport validity, visa requirements, security flags, and health requirements
5. **Results**: The officer is presented with verification results and recommendations

## Deployment Options
For deploying this application to a production environment:

### Option 1: Cloud Hosting with PostgreSQL
1. Export your MySQL database
2. Convert to PostgreSQL format
3. Deploy to a cloud platform like Heroku, Railway, or Render
4. Configure environment variables for database connection

### Option 2: Traditional Hosting
1. Set up a server with Python and MySQL
2. Configure a web server (Nginx/Apache) with WSGI
3. Set up proper security measures

## Important Notes
- Face recognition requires physical access to a camera
- The system requires proper database setup for full functionality
- For testing purposes, use the test accounts provided by administrators

## License
This project is proprietary and confidential. Unauthorized copying, modification, distribution, or use is strictly prohibited.

## Contact
For questions or support, please contact the development team.
