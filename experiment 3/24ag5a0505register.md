<html>
<head>
    <title> Welcome to NNRG e-Book's website</title>
    <script language="javascript">
    // Function to validate the form fields before submitting
    function validate() {
        // Username validation
        var uname = document.forms["f1"]["username"].value;
        if (uname.length == 0) {
            alert("Please Enter UserName");
            document.f1.username.focus();
            return false;
        }
        if (uname.length < 8) {
            alert("Please enter UserName not less than 8 characters");
            document.f1.username.focus();
            return false;
        }

        // Password validation
        var pwd = document.forms["f1"]["password"].value;
        if (pwd.length == 0) {
            alert("Please Enter password");
            document.f1.password.focus();
            return false;
        }
        if (pwd.length < 6) {
            alert("Please enter Password not less than 6 characters");
            document.f1.password.focus();
            return false;
        }

        // Email validation using regex for format
        var email = document.forms["f1"]["email"].value;
        if (email.length == 0) {
            alert("Please Enter email");
            document.f1.email.focus();
            return false;
        } else {
            var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6}$/;
            if (!emailPattern.test(email)) {
                alert("Please enter a valid Email ID");
                document.f1.email.focus();
                return false;
            }
        }

        // Phone number validation (must be a 10-digit number)
        var phno = document.forms["f1"]["phno"].value;
        if (phno.length == 0) {
            alert("Please Enter Phone Number");
            document.f1.phno.focus();
            return false;
        }
        if (isNaN(phno) || phno.length != 10) {
            alert("Please Enter a Valid 10-digit Phone Number");
            document.f1.phno.focus();
            return false;
        }

        // Gender validation (user must choose one gender)
        var genderSelected = false;
        var gender = document.forms["f1"]["gen"];
        for (var i = 0; i < gender.length; i++) {
            if (gender[i].checked) {
                genderSelected = true;
            }
        }
        if (!genderSelected) {
            alert("Please choose a Gender");
            return false;
        }

        // Language validation (user must select at least one language)
        var langSelected = false;
        var languages = document.forms["f1"]["lang"];
        for (var i = 0; i < languages.length; i++) {
            if (languages[i].checked) {
                langSelected = true;
            }
        }
        if (!langSelected) {
            alert("Please select at least one Language option.");
            return false;
        }

        // Address validation (user must enter an address)
        var addr = document.forms["f1"]["address"].value;
        if (addr.length == 0) {
            alert("Please Enter Address");
            document.f1.address.focus();
            return false;
        }

        // If all fields are validated, display success message and return true
        alert("Registration Successful");
        return true;
    }
    </script>
</head>
<body>
    <center><br>
        <h3>Registration Form </h3>
        <br/>
        <!-- Registration form -->
        <form name="f1" onsubmit="return validate()">
        <table cellpadding="1" align="center" >
            <!-- Username field -->
            <tr><td> User Name:*</td>
            <td><input type="text" name="username"></td></tr>
            <!-- Password field -->
            <tr><td>Password:*</td>
            <td><input type="password" name="password"></td></tr>
            <!-- Email field -->
            <tr><td>Email ID:*</td>
            <td><input type="text" name="email"></td></tr>
            <!-- Phone number field -->
            <tr><td>Phone Number:*</td>
            <td><input type="text" name="phno"></td></tr>
            <!-- Gender selection (radio buttons) -->
            <tr><td valign="top">Gender:*</td>
            <td><input type="radio" name="gen" value="Male">Male &nbsp;&nbsp;
            <input type="radio" name="gen" value="Female">Female</td></tr>
            <!-- Language selection (checkboxes) -->
            <tr> <td valign="top">Language Known:*</td>
            <td> <input type="checkbox" name="lang" value="English">English<br/> 
            <input type="checkbox" name="lang" value="Telugu">Telugu<br>
            <input type="checkbox" name="lang" value="Hindi">Hindi<br>
            <input type="checkbox" name="lang" value="Tamil">Tamil
            </td></tr>
            <!-- Address field -->
            <tr> <td valign="top">Address:*</td>
            <td><textarea name="address"></textarea></td>
            <!-- Submit and reset buttons -->
            <tr><td></td><td><input type="submit" value="SUBMIT">
            <input type="reset" value="RESET"></td></tr>
            <!-- Mandatory fields note -->
            <tr> <td colspan=2 >*<font color="#FF0000">fields are mandatory</font>
            </td>
        </table>
        </form>
    </center>
</body>
</html>
