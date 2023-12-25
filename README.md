# Login-Page-code
This is my login page for my vegitable shop app

<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">


    <title>Shoping Vagitable</title>
    <style>
    *{
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }
    body{
        background: rgb(178, 228, 228);

    }
    .row{
        box-shadow:rgba(158, 152, 152, 0.623) ;
        background: rgb(248, 246, 246);
        border-radius: 30px;
        padding-right: -20;
    }
    img{

        border-top-left-radius:30px;
        border-bottom-left-radius:30px;
    }
    .btn1{
        border: none;
        outline: none;
        height: 50px;
        width: 100%;
        background-color: greenyellow;
        color: white;
        border-radius: 4px;
        font-weight: bold;
    }
    .btn1:hover{
        background: rgb(13, 241, 13);
        border: 1px solid;
        color: black;
    }
    .fa-envelope-o{
        position: relative;
    }
    .fa{
        position: absolute;
        right: 10px;
        margin-top: 10px;
        cursor: pointer;
    }
    .col-lg-7{
        position: relative;
    }
    .fa{
        position: absolute;
        right: 10px;
        margin-top: 10px;
        cursor: pointer;
    }
    .form #email_error,
    .form #password_error{
    margin-top: 5px;
    width: 345px;
    font-size: 18px;
    color: #c62828;
    background: rgba(255,0,0,0,1);
    text-align: center;
    padding: 5px 8px;
    border-radius: 3px;
    border: 1px solid #ef9a9a;
    display: none;
    }

</style>

    </head>
    <body>
    <section class="form my-4 mx-5"   >
        <div class="container">
            <div class="row no-gutters">
                <div class="col-lg-7">
                    <img src="./img.jpg" class="img-fluid" alt="">
                </div>
                <div class="col-lg-5 px-4 pt-4">
                    <h1 class="font-weight-bold py-3">VEGETABLE STORE</h1>
                    <h4>Sign into your Account?</h4>
                    <form>
                        <div class="form-row" v-if="!submitted" >
                            <div class="col-lg-7" >
                                <i class="fa fa-envelope-o" aria-hidden="true"></i>
                                <input type="Email" placeholder="Enter email" class="form-control my-2 pt-1"  required><div class="forms-inputs mb-4"> <v-model="email" v-bind:class="{'form-control':true, 'is-invalid' : !validEmail(email) && emailBlured}" v-on:blur="emailBlured = true">
                                <div class="invalid-feedback"> email is required!</div>
                                </div >
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="col-lg-7">
                                <i class="fa fa-eye-slash"  id="eye" aria-hidden="true"></i>
                                 <input type="password" class="form-control my-2 " placeholder="Enter Password" id="passfield" required>
                                 <div class="invalid-feedback">Password must be 8 character!</div>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="col-lg-7">
                               <button type="submit" class="btn1">Login</button>
                            </div>
                        </div>
                        <a href="forgotten.html">forgot password</a>
                        <p>Don't have an Account?<a href="re    gistration.html">Register Here</a></p>
                    </form>
                </div>
            </div>
        </div>
    </section>

     <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.10.2/dist/umd/popper.min.js" integrity="sha384-7+zCNj/IqJ95wo16oMtfsKbZ9ccEh31eOz1HGyDuCQ6wgnyJNSYdrPa03rtR1zdB" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.min.js" integrity="sha384-QJHtvGhmr9XOIpI6YVutG+2QOK9T+ZnN4kzFN1RtK3zEFEIsxhlmWl5/YESvpZ13" crossorigin="anonymous"></script>
    -->
    <script>
        document.getElementById("eye").addEventListener("click",function(){
         if(document.getElementById("passfield").type=="password"){
            document.getElementById("passfield").type="text";
            this.classList.add("fa-eye");
            this.classList.remove("fa-eye-slash");
         }else{
            document.getElementById("passfield").type="password"
            this.classList.remove("fa-eye");
            this.classList.add("fa-eye-slash");
         }
        });

    </script>

  </body>
</html>
