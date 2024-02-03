# Basic-Form-Making
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-image: url(bgImg.jpg);
            background-size: auto;
        }
        form{
            color: black;
            background-color: rgba(0, 0, 0, 0.086);
            border: 2px solid gray;
            padding: 20px;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
        }

        input{
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 5px;
            padding: 5px;
        }

        textarea{
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 10px;
            padding: 5px;
        }
        button {
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 10px;
            padding: 5px;
            background-color: rgba(128, 128, 128, 0.462);
        }

        #head {
            display: flex;
            justify-content: center;
        }

    </style>
</head>
<body>

    <form>
        <h2 Id="head">LOGIN</h2>

        <label for="name">First Name</label>
        <input type="text"id="name" placeholder="first name" pattern="[A-Za-z]+" required>
       
        <label for="lastName">Last Name</label>
        <input type="text" id="lastName" placeholder="last name" pattern="[A-Za-z]+" required>
        
        <label for="email">Email</label>
        <input type="email" id="email" required> 
       
        <label for="address">Address</label>
        <textarea rows="4" cols="50" id="address" placeholder="home address..." required></textarea> 
        <!-- <input type="text" placeholder="home address..."> -->
      
        <label for="number">PhoneNumber</label>
        <input type="number" id="number" pattern="[0-9]+" required> 
       
        <label for="gender">Gender
        <input type="radio" value="male" >Male 
        <input type="radio" value="female" >Female
        <input type="radio" value="other"> Other
        </label>

        <label for="password">Password</label>
        <input type="password" id="password" minlength="8" required>
        
        <button type="button" onclick="submitForm()">Submit</button>
        
    </form>
    <footer id="button">
    </footer>

    <script>
        function submitForm() {
            if (validateForm()){
                setTimeout(function() {
                    alert("Welcome! Your form has been submitted successfully.")
                },1000);
            }
        }

        function validateForm() {
            var name = document.getElementById("name").value;
            var lastName = document.getElementById("lastName").value;

            if(!/^[A-Za-z]+$/.test(name) || !/^[A-Za-z]+$/.test(lastName)){
                alert("Please enter valid first and last name.");
                return false;
            }
            var email = document.getElementById("email").value;
            if(email == "" || !/^.+@.+\..+$/.test(email)){
                alert("Please enter a valid email address");
                return false;
            } 

            var password = document.getElementById("password").value;
            if(password.length > 8){
                alert("password must be 8 characters long.");
                return false;
            }
            if(password.length < 8){
                alert("password is too short.");
                return false;
            }

            

            return true;
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-image: url(bgImg.jpg);
            background-size: auto;
        }
        form{
            color: black;
            background-color: rgba(0, 0, 0, 0.086);
            border: 2px solid gray;
            padding: 20px;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
        }

        input{
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 5px;
            padding: 5px;
        }

        textarea{
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 10px;
            padding: 5px;
        }
        button {
            margin-bottom: 20px;
            margin-top: 5px;
            border-radius: 10px;
            padding: 5px;
            background-color: rgba(128, 128, 128, 0.462);
        }

        #head {
            display: flex;
            justify-content: center;
        }

    </style>
</head>
<body>

    <form>
        <h2 Id="head">LOGIN</h2>

        <label for="name">First Name</label>
        <input type="text"id="name" placeholder="first name" pattern="[A-Za-z]+" required>
       
        <label for="lastName">Last Name</label>
        <input type="text" id="lastName" placeholder="last name" pattern="[A-Za-z]+" required>
        
        <label for="email">Email</label>
        <input type="email" id="email" required> 
       
        <label for="address">Address</label>
        <textarea rows="4" cols="50" id="address" placeholder="home address..." required></textarea> 
        <!-- <input type="text" placeholder="home address..."> -->
      
        <label for="number">PhoneNumber</label>
        <input type="number" id="number" pattern="[0-9]+" required> 
       
        <label for="gender">Gender
        <input type="radio" value="male" >Male 
        <input type="radio" value="female" >Female
        <input type="radio" value="other"> Other
        </label>

        <label for="password">Password</label>
        <input type="password" id="password" minlength="8" required>
        
        <button type="button" onclick="submitForm()">Submit</button>
        
    </form>
    <footer id="button">
    </footer>

    <script>
        function submitForm() {
            if (validateForm()){
                setTimeout(function() {
                    alert("Welcome! Your form has been submitted successfully.")
                },1000);
            }
        }

        function validateForm() {
            var name = document.getElementById("name").value;
            var lastName = document.getElementById("lastName").value;

            if(!/^[A-Za-z]+$/.test(name) || !/^[A-Za-z]+$/.test(lastName)){
                alert("Please enter valid first and last name.");
                return false;
            }
            var email = document.getElementById("email").value;
            if(email == "" || !/^.+@.+\..+$/.test(email)){
                alert("Please enter a valid email address");
                return false;
            } 

            var password = document.getElementById("password").value;
            if(password.length > 8){
                alert("password must be 8 characters long.");
                return false;
            }
            if(password.length < 8){
                alert("password is too short.");
                return false;
            }

            

            return true;
        }
    </script>
</body>
</html>
