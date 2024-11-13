<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Project Management System</title>
    <style>
        /* CSS styling */
        body {
            font-family: Arial, sans-serif;
            background-color: #f8f9fa;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 10px;
            text-decoration: none;
        }
        h2 {
            color: #007bff;
        }
        main, .form-container {
            max-width: 500px;
            margin: 20px auto;
            padding: 1em;
            background: #ffffff;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        label {
            margin-top: 1em;
            display: block;
            text-align: left;
        }
        input, button {
            width: 100%;
            padding: 0.5em;
            margin-top: 0.5em;
            font-size: 1em;
        }
        .hidden {
            display: none;
        }
        .dashboard-content {
            text-align: left;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>Student Project Management System</h1>
        <nav>
            <a href="#" onclick="showPage('home')">Home</a>
            <a href="#" onclick="showPage('login')">Login</a>
        </nav>
    </header>

    <!-- Main Content (Home Page) -->
    <main id="home">
        <h2>Welcome to the Student Project Management System</h2>
        <p>This system helps allocate and manage student projects efficiently. Log in to access your dashboard and manage projects.</p>
    </main>

    <!-- Login Form -->
    <div id="login" class="form-container hidden">
        <h2>Login</h2>
        <form onsubmit="return validateForm()">
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required>
            
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>
            
            <button type="submit">Login</button>
        </form>
    </div>

    <!-- Dashboard -->
    <div id="dashboard" class="form-container hidden">
        <h2>Dashboard</h2>
        <p>Enter Student Project Details:</p>
        <form id="studentForm" onsubmit="return addStudent()">
            <label for="studentName">Name:</label>
            <input type="text" id="studentName" name="studentName" required>
            
            <label for="department">Department:</label>
            <input type="text" id="department" name="department" required>
            
            <label for="matricNo">Matric No:</label>
            <input type="text" id="matricNo" name="matricNo" required>
            
            <label for="level">Level:</label>
            <input type="text" id="level" name="level" required>
            
            <label for="projectTopic">Project Topic:</label>
            <input type="text" id="projectTopic" name="projectTopic" required>
            
            <button type="submit">Submit</button>
        </form>
        
        <div id="studentList" class="dashboard-content">
            <h3>Student Project List</h3>
            <ul id="studentData"></ul>
        </div>
    </div>

    <script>
        // JavaScript for page navigation and form validation
        function showPage(pageId) {
            document.getElementById("home").classList.add("hidden");
            document.getElementById("login").classList.add("hidden");
            document.getElementById("dashboard").classList.add("hidden");
            document.getElementById(pageId).classList.remove("hidden");
        }

        function validateForm() {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            if (username && password) {
                alert("Login successful! Redirecting to dashboard...");
                showPage('dashboard'); // Redirect to dashboard
                return false;
            }
            alert("Please enter both username and password.");
            return false;
        }

        function addStudent() {
            const name = document.getElementById("studentName").value;
            const department = document.getElementById("department").value;
            const matricNo = document.getElementById("matricNo").value;
            const level = document.getElementById("level").value;
            const projectTopic = document.getElementById("projectTopic").value;

            // Display student details in the list
            const studentData = document.getElementById("studentData");
            const studentItem = document.createElement("li");
            studentItem.textContent = `${name} | ${department} | ${matricNo} | ${level} | ${projectTopic}`;
            studentData.appendChild(studentItem);

            // Clear form after submission
            document.getElementById("studentForm").reset();

            return false; // Prevent form submission
        }
    </script>

</body>
</html>
