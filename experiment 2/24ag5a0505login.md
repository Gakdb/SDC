<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login - FBS</title>

    <!-- Bootstrap CSS (Latest Version) -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
        /* Set background color for the entire page */
        body {
            background-color: #f4f4f4;
        }

        /* Footer Styling */
        footer {
            background-color: #333; /* Dark background */
            color: white; /* White text */
            text-align: center;
            padding: 10px;
            position: fixed; /* Stick to the bottom */
            bottom: 0;
            width: 100%;
        }

        /* Wrapper to add spacing around content */
        .wrapper {
            margin-top: 20px;
        }

        /* Styling for the login form container */
        .form-container {
            background-color: white;
            padding: 40px;
            border-radius: 5px; /* Rounded corners */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Adds a shadow effect */
        }
    </style>
</head>
<body>

    <div class="wrapper">
        <!-- Header Section -->
        <div class="container">
            <header class="my-4">
                <div class="row">
                    <!-- Logo Column (Left) -->
                    <div class="col-3">
                        <img src="fbs.png" alt="FBS LOGO" class="img-fluid" width="130" height="100"/>
                    </div>
                    <!-- Title Column (Right) -->
                    <div class="col-9 text-center bg-dark p-3">
                        <h1 class="text-white">FBS - WORLD BEST ONLINE EBOOKS WEBSITE</h1>
                    </div>
                </div>
            </header>
        </div>

        <!-- Navigation Bar -->
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <div class="container">
                <!-- Website Name -->
                <a class="navbar-brand" href="#">FBS</a>
                
                <!-- Navbar Toggler for Mobile -->
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <!-- Navigation Links -->
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav mx-auto">
                        <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
                        <li class="nav-item"><a class="nav-link active" href="login.html">Login</a></li>
                        <li class="nav-item"><a class="nav-link" href="registration.html">Registration</a></li>
                        <li class="nav-item"><a class="nav-link" href="cart.html">Cart</a></li>
                    </ul>
                </div>
            </div>
        </nav>

        <!-- Login Form Section -->
        <div class="container my-5">
            <div class="form-container mx-auto col-md-6">
                <h3 class="text-center mb-4">Login</h3>
                <!-- Login Form -->
                <form action="login-process.php" method="post">
                    <!-- Username Input Field -->
                    <div class="form-group">
                        <label for="username">User Name</label>
                        <input type="text" class="form-control" id="username" name="username" required>
                    </div>
                    <!-- Password Input Field -->
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" class="form-control" id="password" name="password" required>
                    </div>
                    <!-- Submit Button -->
                    <button type="submit" class="btn btn-primary btn-block">Login</button>
                </form>
            </div>
        </div>

        <!-- Footer Section -->
        <footer>
            <p>(C) 2024 All rights reserved by FBS ebooks</p>
        </footer>
    </div>

    <!-- Bootstrap JavaScript (Required for Navbar and Other Components) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>
