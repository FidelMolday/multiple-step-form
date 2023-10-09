This is js repostory
<!DOCTYPE HTML>
<html>
    <head>
        <title>Progressive Form / Multi steps form</title>
    </head>
    <body>
       <div class="container">
         <form id="Form1">
            <h3>CREATE ACCOUNT</h3>
            <input type="text" placeholder="Email" required>
            <input type="password" placeholder="Password" required>
            <input type="password" placeholder="Confirm Password" required>
         <div class="btn-box">
            <button type="button" id="Next1">Next</button>
         </div>
         </form>
         <form id="Form2">
            <h3>SOCIAL LINKS</h3>
            <input type="text" placeholder="Medium">
            <input type="text" placeholder="Github">
            <input type="text" placeholder="Linkedin">
         <div class="btn-box">
            <button type="button" id="Back1">Back</button>
            <button type="button" id="Next2">Next</button>
         </div>
         </form>
         <form id="Form3">
            <h3>PERSONAL INFO</h3>
            <input type="text" placeholder="First Name" required>
            <input type="text" placeholder="Last Name" required>
            <input type="text" placeholder="Mobile No." required>
         <div class="btn-box">
            <button type="button" id="Back2">Back</button>
            <button type="submit">Submit</button>
         </div>
         </form>
         <div class="step-row">
            <div id="progress"></div>
             <div class="step-col"><small>Step 1</small></div>
             <div class="step-col"><small>Step 2</small></div>
             <div class="step-col"><small>Step 3</small></div>
         </div>
       </div>   

       <style>
        *{
          margin: 0;
          padding: 0;
          font-family: sans-serif;
        }
        body{
            background-image: linear-gradient(rgba(0,0,0,0.8),rgba(0,0,0,0.8));
            background-size: cover;
            background-position: center;
        }
        .container{
            width: 360px;
            height: 400px;
            margin: 8% auto;
            background: #fff;
            border-radius: 5px;
            position: relative;
            overflow: hidden;
        }
        h3{
            text-align: center;
            margin-bottom: 40px;
            color: #777;
        }
        .container form{
            width: 280px;
            position: absolute;
            top: 100px;
            left: 40px;
            transition: 0.5s;
        }
        form input{
            width: 100%;
            padding: 10px 5px;
            margin: 5px 0;
            border: 0;
            border-bottom: 1px solid #999;
            outline: none;
            background: transparent;
        }
        .btn-box{
            width: 100%;
            margin: 30px auto;
            text-align: center;
        }
        form button{
            width: 110px;
            height: 35px;
            margin: 0 10px;
            background: linear-gradient(to right,#ff105f,#ffad06);
            border-radius: 30px;
            border: 0;
            outline: none;
            color: #fff;
            cursor: pointer;
        }
        #Form2{
            left: 450px;
        }
        #Form3{
            left: 450px;
        }
        .step-row{
            width: 360px;
            height: 40px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            box-shadow: 0 -1px 5px -1px #000;
            position: relative;
        }
        .step-col{
            width: 120px;
            text-align: center;
            color: #333;
            position: relative;
        }
        #progress{
            position: absolute;
            height: 100%;
            width: 120px;
            background: linear-gradient(to right,#ff105f,#ffad06);
            transition: 1s;
        }
        #progress::after{
            content: '';
            height: 0;
            width: 0;
            border-top: 20px solid transparent;
            border-bottom: 20px solid transparent;
            position: absolute;
            right: -20px;
            top: 0;
            border-left: 20px solid #ffad06;
        }
       </style>
       <script>
         var Form1 = document.getElementById("Form1");
         var Form2 = document.getElementById("Form2");
         var Form3 = document.getElementById("Form3");

         var Next1 = document.getElementById("Next1");
         var Next2 = document.getElementById("Next2");
         var Back1 = document.getElementById("Back1");
         var Back2 = document.getElementById("Back2");
          
         var progress = document.getElementById("progress");

         Next1.onclick = function(){
            Form1.style.left = "-450px";
            Form2.style.left = "40px";
            progress.style.width = "240px";
         }
         Back1.onclick = function(){
            Form1.style.left = "40px";
            Form2.style.left = "450px";
            progress.style.width = "120px";
         }
         Next2.onclick = function(){
            Form2.style.left = "-450px";
            Form3.style.left = "40px";
            progress.style.width = "360px";
         }
         Back2.onclick = function(){
            Form2.style.left = "40px";
            Form3.style.left = "450px";
         }
       </script>
    </body>
</html>
