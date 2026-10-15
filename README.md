<div align="center">
  <h1>OptiRH - Human Resources Management</h1>
</div>

<div align="center">
  <a href="https://github.com/hamdikbell/OptiRh-Web-Desktop.git" target="_blank">
    <img src="https://github.com/user-attachments/assets/0f3bdb15-6321-42da-b294-c12b76d025d3" width="200" alt="OptiRH Logo">
  </a>
</div>


<p align="center">
  Developed by the <strong>Nexus Team</strong>
</p>

---

## 📌 Project Overview

**OptiRH** is an innovative Human Resources Management solution combining a **JavaFX desktop application** and a **web platform built with Symfony**.  
The project aims to **simplify, automate, and optimize** HR management for companies of all sizes.

The **web version** provides centralized, digitalized HR management accessible from any modern browser.

---

## 🚀 Main Features

- **User Management** (Ahmed Trabelsi)  
  - Creation and management of user accounts with roles and permissions
  - Secure authentication and access control

- **Offer & Demand Module** (Mariem Jlassi)  
  - Publish and track job and internship offers
  - Advanced search and filtering options
  - Email notifications for confirmations

- **Event Module** (Ikbel Hamdi)  
  - **Event location displayed on maps** for better navigation  
  - **Weather forecast integration** to choose the best timing for events  
  - **SMS confirmation** for participants  
  - **Stripe payment integration** for event tickets  
  - **AI-generated event descriptions** based on title, date, and modality  
  - Download and **print tickets with barcode/QR code**  
  - Integrated **event calendar** for planning and overview

- **Complaint Module** (Maram Rachdi)  
  - Structured complaint tracking
  - Automatic ticket analysis using AI

- **Transport Module** (Linda Jenhani)  
  - Manage and reserve employee transportation
  - Optimized interface for web usability

- **Mission Module** (Oumayma Bouhani)  
  - Assign and track tasks and projects
  - Accessible via the back-office web interface

---

## 🎯 Project Objectives

- **Advanced Automation**: Reduce manual work and human errors via automated HR processes.  
- **Data Centralization**: Secure and centralized access to HR information through the web platform.  
- **Accessibility & Usability**: Modern, intuitive interface accessible via browser.  
- **Scalability**: Adaptable for SMEs and large enterprises, with extensible functionalities.

---

## 🛠️ Technologies Used

- **Frontend**: Symfony (web) and JavaFX (desktop)  
- **Backend**: PHP (Symfony)  
- **Database**: MySQL  
- **Security**: Authentication and secure access management (JWT, OAuth, etc.)  
- **Task Management**: Symfony Workflow for validation and assignment processes  

---

## 📖 Installation & Configuration

### Prerequisites

- PHP 8.0+  
- Symfony 5.x+  
- Composer  
- MySQL Server  
- Node.js (for frontend assets)  
- JDK 17+ (for JavaFX desktop app)  

### Installation Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/hamdikbell/OptiRh-Web-Desktop.git
   cd OptiRH
   ```

2. **Install PHP dependencies**

   ```bash
   composer install
   ```

3. **Install frontend dependencies**

   ```bash
   npm install
   npm run build
   ```

4. **Configure environment**

   - Copy .env to .env.local` :

     ```bash
     cp .env .env.local
     ```

   - Edit .env.local to set database connection: for exemple :

     ```env
     DATABASE_URL="mysql://utilisateur:mot_de_passe@localhost:3306/optirh_db"
     ```

   
5. **Create the database**

   ```bash
   php bin/console doctrine:database:create
   ```

6. **Run migrations**

   ```bash
   php bin/console doctrine:migrations:migrate
   ```

7. **Start the development server**

   ```bash
   symfony server:start
   ```

8. **Set up the JavaFX desktop application**

     1. **Clone the repository**
      ```bash
          git clone https://github.com/hamdikbell/OptiRh-Web-Desktop.git
          cd OptiRH
      ```
    2. **Configure database in application.properties**
       - Create a database named  `optirh_db`
       - Set the database connection parameters in `application.properties`
    
    3. **Build and run**
      ```bash
          mvn clean install
          mvn javafx:run
      ```

### ✅ Post-Installation Checks

- Access the web interface at `http://localhost:8000` to ensure the application is working correctly.
- Test authentication and main features (user management, offers, events, etc.).
- Check logs (`var/log/dev.log`) for any errors.

## 📌 UML Diagrams & Style Guide

- **UML Diagrams**: Define roles (Administrator, Project Manager, Employee, etc.)
- **Style Guide**:  
  - **Colors**: Navy & Turquoise (stability and dynamism)  
  - **Typography**: Roboto (clarity and modernity)  
  - **UX/UI**: Smooth and intuitive navigation

## 📝 Additional Notes

- For a production environment, configure a web server such as **Nginx** or **Apache**, and ensure proper permissions for the `var/` and `public/` directories.
- Enable real-time notifications by configuring a messaging service (e.g., Mercure or WebSocket) if needed.
- For advanced features such as AI-powered complaint analysis, integrate a third-party service (e.g., AI API or a local AI model).

*OptiRH – Simplify your Human Resources Management with a modern and intuitive solution!*