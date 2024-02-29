<?php 
    //registrazione
    session_start();
    $username = $email = $password = "";
    $no_user = $err_email = $no_psw = $not_secure = "";
    $user = $pass = '';
    $errorUser = $errorPassword = '';
    
    function pulisciInput($dato) {
        $dato = trim($dato);
        $dato = stripslashes($dato);
        $dato = htmlspecialchars($dato);
    
        return $dato;
    }

    if ($_SERVER['REQUEST_METHOD'] == 'POST') {
        // registrazione
        if (isset($_POST['registration-submit'])) {
            if (!empty($_POST['User'])) {
                $username = pulisciInput($_POST['User']);
                $_SESSION['username'] = $username;
            } else {
                $no_user = "User mancante";
            }
            
            if (!empty($_POST['Email'])) {
                $email = pulisciInput($_POST['Email']);
                if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
                    $err_email = "Email non valida";
                }
            } else {
                $err_email = "Email mancante";
            }
            
            if (!empty($_POST["Password"])) {
                $password = pulisciInput($_POST['Password']);
                if (!preg_match('/^(?=.*\d)(?=.*[@#\-_$%^&+=§!\?])(?=.*[a-z])(?=.*[A-Z])[0-9A-Za-z@#\-_$%^&+=§!\?]{8,20}$/', $password)) {
                    $no_psw = 'La password non rispetta i criteri di sicurezza ';
                }
            } else {
                $no_psw = 'Password mancante ';
            }
            if ($no_user == '' && $err_email == '' && $no_psw == ''){
                $servername = "localhost"; 
                $usernameDB = "root"; 
                $passwordD = ""; 
                $db="sitodb"; 
                $conn = mysqli_connect($servername, $usernameDB, $passwordD, $db);
                if (!$conn) { 
                    die("Connection failed: " . mysqli_connect_error()); 
       
             } 
                $sql="INSERT INTO utente (username, email, password) VALUES ('$username', '$email', '$password')"; 
                
                if (!mysqli_query($conn, $sql)) {
                    echo "Errore di connessione"; 
                    }
                mysqli_close($conn);
                header("location: ./landing.php?registrazione=OK");
            }
        }

        // login
        if (isset($_POST['login-submit'])) {
            if (!empty($_POST["username"])) {
                $user = $_POST["username"];
            } else {
                $errorUser = '<span style="color: red;">Username mancante</span>';
            }
            if (!empty($_POST["password"])) {
                $pass = $_POST["password"];
            } else {
                $errorPassword = '<span style="color: red;">Password mancante</span>';
            }
            if ($user != '' && $pass != '') {
                $_SESSION['username'] = $user;
                $servername = "localhost"; 
                $usernameDB = "root"; 
                $passwordD = ""; 
                $db="sitodb";
                $conn = mysqli_connect($servername, $usernameDB, $passwordD, $db);
                if (!$conn) {
                    die("Connection failed: " . mysqli_connect_error()); 
                } 
                $query= "SELECT * FROM utente WHERE username= '$user' AND password= '$pass'"; 
                $result = mysqli_query($conn, $query); //esegue l’interrogazione 
                if (mysqli_num_rows($result) > 0) {
                    header("location: ./HomePage.php"); 
                    exit();
                }else {
                    header("location: ./landing.php?ACCESSO_FALLITO");
                    exit();
                }
                mysqli_close($conn);
            }
        }
    }
?>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <link rel="stylesheet" href="./style/styleLogin.css">
    <title>Login</title>
    <link rel="website icon" type="png" href="./img/logoSito.png">
</head>

<body>

    <div class="container" id="container">
        <div class="form-container sign-up">
            <form action="<?php echo $_SERVER["PHP_SELF"];?>" method="post" id="registration-form">
                <h1>Create Account</h1>
                <div class="social-icons">
                    <a href="#" class="icon"><i class="fa-brands fa-google-plus-g"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-github"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-linkedin-in"></i></a>
                </div>
                    <input type="text" placeholder="Username" id="User" name="User" value="<?php echo "$username"; ?>">
                    <span class="error-message"><?php echo $no_user; ?></span>
                    
                    <input type="text" placeholder="Email" id="Email" name= "Email" value="<?php echo "$email"; ?>">
                    <span class="error-message"><?php echo $err_email; ?></span>
                    
                    <input type="password" placeholder="password" id="Password" name= "Password" value="<?php echo "$password"; ?>">
                    <span class="error-message"><?php echo $no_psw; ?></span>
                    
                    <input type="submit" name="registration-submit" value="INVIO">
        </form>
    </div>

        <div class="form-container sign-in">
            <form name="form_login" method="post" action="<?php echo $_SERVER["PHP_SELF"];?>">
                <h1>Sign In</h1>
                <div class="social-icons">
                    <a href="#" class="icon"><i class="fa-brands fa-google-plus-g"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-github"></i></a>
                    <a href="#" class="icon"><i class="fa-brands fa-linkedin-in"></i></a>
                    </div>
                    <input type="text" placeholder="User" name="username" value="<?php echo "$user"; ?>">
                    <span class="error-message"><?php echo $errorUser; ?></span>
                    
                    <input type="password" placeholder="Password" name= "password" value="<?php echo "$pass"; ?>">
                    <span class="error-message"><?php echo $errorPassword; ?></span>
                    
                    <a href="#">Password dimenticata?</a>
                    <input type="submit" name="login-submit" value="INVIO">
        </form>
    </div>
        <div class="toggle-container">
            <div class="toggle">
                <div class="toggle-panel toggle-left">
                    <h1>Benvenuto!</h1>
                    <p>Inserisci i tuoi dati per accedere al sito</p>
                    <button class="hidden" id="login">Sign In</button>
                </div>
                <div class="toggle-panel toggle-right">
                    <h1>Bentornato, Amico!</h1>
                    <p>Inserisci i tuoi dati per accedere al sito</p>
                    <button class="hidden" id="register">Sign Up</button>
                </div>
            </div>
        </div>
    </div>

    <script>
        const container = document.getElementById("container");
        const registerBtn = document.getElementById("register");
        const loginBtn = document.getElementById("login");
        const contactForm = document.querySelector(".contact-form");
        const username = document.querySelector("#username");
        const password = document.querySelector("#password");
        registerBtn.addEventListener("click", () => {
        container.classList.add("active");
        });
        loginBtn.addEventListener("click", () => {
        container.classList.remove("active");
        });

        contactForm.addEventListener("submit", submitForm);

        function submitForm(e) {
        e.preventDefault();

        const usernameValue = username.value;
        const passwordValue = password.value;

        if (username === "") {
            username.style.border = "2px solid red";
        }

        if (password === "") {
            password.style.border = "2px solid red";
        }
        }
    </script>
</body>

</html>
