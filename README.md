# 🎓 Online Course Management System (JSP + Maven + MySQL)

A complete Learning Management System built using **JSP, Servlets, JDBC, MySQL, and Maven**.  
This project allows students to browse courses, enroll, view course details, upload assessments, and manage their profile.

---

## 🚀 Features

### 👤 Student Features
- Student Registration & Login (with session handling)
- Student Dashboard / Profile Page
- View personal details
- View list of enrolled courses
- Edit profile (optional)
- Logout functionality

### 📚 Course Features
- Browse all available courses
- View detailed course pages:
  - Modules
  - Notes
  - Assignments
  - Marks
  - Assessment upload section
- Enroll in a course
- Prevent duplicate enrollment
- View list of enrolled courses

### 🗂 Admin (optional future)
- Upload notes
- Upload assignments
- Manage students
- Manage courses

---

## 🛠 Technologies Used

| Layer              | Technology         |
|-------------------|--------------------|
| Frontend UI       | HTML, CSS, JSP     |
| Backend Logic     | JSP + Java + JDBC  |
| Database          | MySQL              |
| Build Tool        | Maven              |
| Server            | Apache Tomcat 9    |
| IDE               | IntelliJ IDEA      |

---

## 📦 Project Structure

```
src/
 └── main/
     ├── java/                # Backend logic (if using servlets)
     ├── webapp/
     │     ├── studentLogin.jsp
     │     ├── studentRegister.jsp
     │     ├── studentProfile.jsp
     │     ├── browseCourses.jsp
     │     ├── myCourses.jsp
     │     ├── enroll.jsp
     │     ├── courseDetail pages (java, ads, ml, etc.)
     │     ├── CSS files
     │     └── WEB-INF/
     │           └── web.xml
 ├── pom.xml
 └── .gitignore
```

---

## 💾 Database Structure (MySQL)

### Table: `students`
```
id (INT) PK
name VARCHAR(100)
email VARCHAR(100)
password VARCHAR(50)
```

### Table: `student_course`
```
id INT PK
student_id INT FK
course_name VARCHAR(200)
course_code VARCHAR(20)
```

You may add more tables for:
- submissions
- notes
- assignments
- admin

---

## 🔧 Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/online-course-management-system.git
```

### 2. Import in IntelliJ as **Maven Project**

### 3. Configure Database
Update your `dbconnect.jsp`:

```jsp
<%
Class.forName("com.mysql.cj.jdbc.Driver");
Connection conn = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/yourdbname",
    "root",
    "yourpassword"
);
%>
```

### 4. Run the project on Tomcat
- Add Tomcat configuration
- Deploy `war exploded`
- Start server
- Open `http://localhost:8080/your-project/studentLogin.jsp`

---

## 📸 Screenshots (Add your images here)

Place screenshots inside a folder:

```
/screenshots
```

Example:

```
![Login Page](screenshots/login.png)
![Profile Page](screenshots/profile.png)
![Courses Page](screenshots/courses.png)
```

---

## 🧠 Future Enhancements
- Admin Panel
- Student Progress Tracking
- Quiz Module
- Certificate Generation
- Discussion Forum
- Course Completion Indicator

---

## 🙌 Contributors
Made by **Pragya(202401100400135) and Mahima(202401100400116)** 
cse-aiml-b

 

---

## 📄 License
This project is for educational use.

