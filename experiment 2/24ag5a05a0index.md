<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home - FBS</title>

    <!-- Link to Bootstrap CSS for styling -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">

    <style>
        /* Styling for the hero section */
        .hero-section {
            margin-top: 30px; /* Adds space at the top */
            padding: 20px; /* Adds padding for better spacing */
        }

        /* Styling for the footer */
        footer {
            background-color: #333; /* Dark background for footer */
            color: white; /* White text for contrast */
            text-align: center; /* Centers the text */
            padding: 10px; /* Adds padding */
            position: fixed; /* Fixes the footer at the bottom */
            bottom: 0; /* Positions the footer at the bottom */
            width: 100%; /* Makes it full-width */
        }
    </style>
</head>
<body>

    <div class="wrapper">
        <!-- Header Section -->
        <div class="container">
            <header class="my-4">
                <div class="row">
                    <!-- Logo Section -->
                    <div class="col-3">
                        <img src="fbs.png" alt="FBS LOGO" class="img-fluid" width="130" height="100"/>
                    </div>
                    <!-- Website Title -->
                    <div class="col-9 text-center bg-dark p-3">
                        <h1 class="text-white">FBS - WORLD BEST ONLINE EBOOKS WEBSITE</h1>
                    </div>
                </div>
            </header>
        </div>

        <!-- Navigation Bar -->
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <div class="container">
                <ul class="navbar-nav mx-auto">
                    <!-- Navigation Links -->
                    <li class="nav-item"><a class="nav-link active" href="index.html">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="login.html">Login</a></li>
                    <li class="nav-item"><a class="nav-link" href="registration.html">Registration</a></li>
                    <li class="nav-item"><a class="nav-link" href="cart.html">Cart</a></li>
                </ul>
            </div>
        </nav>

        <!-- Hero Section -->
        <div class="container hero-section text-center">
            <h2>Welcome to FBS e-Book's Website</h2>
            <p>
                Shopping at <span class="fw-bold fs-4">FBS</span> can be both 
                <span class="fw-bold fs-4">fun</span> and 
                <span class="fw-bold fs-4">savings</span>.
            </p>
            <p>
                Shop with us in this special <span class="fw-bold fs-4">discount</span> season and save up to 
                <span class="fw-bold fs-4">90%</span> on all your purchases.
            </p>
        </div>

        <!-- Footer Section -->
        <footer>
            <p>(C) 2024 All rights reserved by FBS ebooks</p>
        </footer>
    </div>

    <!-- Bootstrap JavaScript (for responsive features, dropdowns, etc.) -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.0.7/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

</body>
</html>
