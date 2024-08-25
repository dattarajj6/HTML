<!-- calculaotor
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form </title>
</head>
<body>
    <form>
    <center>
    <h1>javascript Operation</h1>
    1st Number:<input type="text" id="firstNumber"> <br> <br>
    2st Number:<input type="text" id="secondNumber"> <br> <br>
    <label> Select Operators</label>
    <label> Basic Operators</label>
    <input type="button" onclick="addBy()" value="+"/>
    <input type="button" onclick="multiplyBy()" value="*"/>
    <input type="button" onclick="subBy()" value="-">
    <input type="button" onclick="divBy()" value="/">
    <br><br>

    <label> Assignment Operators :</label>
    <input type="button" onclick="Assignment()" value="=+"><br><br>

    <label> Comparison Operators :</label>
    <input type="button" onclick="Comparison()" value="=="><br><br>

    <label> Relational Operators :</label>
    <input type="button" onclick="Relational()" value=">="><br><br>

    <label>Logical Operators</label>
    <input type="button" onclick="Logical()" value="||"><br><br>
    <hr>
    <p> The Result is:
        <span id="result"></span>
    </p>
</center>
</form>
<script>
    function addBy(){
        num1= parseInt(document.getElementById("firstNumber").value);
        num2= parseInt(document.getElementById("secondNumber").value);
        document.getElementById("result").innerHTML=num1+num2;
    }
    function multiplyBy(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumber").value;
        document.getElementById("result").innerHTML=num1*num2;
    }
    function subBy(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumber").value;
        document.getElementById("result").innerHTML=num1-num2;
    }
    function divBy(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumber").value;
        document.getElementById("result").innerHTML=num1/num2;
    }

    function Assignment(){
        num1= parseInt(document.getElementById("firstNumber").value);
        num2= parseInt(document.getElementById("secondNumber").value);
        document.getElementById("result").innerHTML=num=+num2;
    }
    function Comparison(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumberr").value;
        document.getElementById("result").innerHTML=num1!=num2;
    }
    function Relational(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumber").value;
        document.getElementById("result").innerHTML=num1>num2;
    }

    function Logical(){
        num1= document.getElementById("firstNumber").value;
        num2= document.getElementById("secondNumber").value;
        document.getElementById("result").innerHTML=num1+num2 || num1+num2;
    }
    
</script>

</body>
</html>
-->




<!-- form validationn

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>log</title>
</head>
<body>
    <h2>Login page</h2>
    <form>
        Name:
        <input type="text" id="txtname" required placeholder="Enter Name" value="">
        <br><br>
        Mobile number:
        <input type="number" id="num" required placeholder="Enter mobile number" value="">
        <br><br>
        password:
        <input type="password" id="pwd" required placeholder="Enter password" value="">
        <br><br>

        Confirm password:
        <input type="password" id="cpwd" required placeholder="Re-type the password" value="">
        <br><br>
        <input type="button" id="btn" value="submit" onclick="fnDisplay()">
    </form>
    <script>
        function fnDisplay(){
            var v1=document.getElementById("txtname").value;
            var v2=document.getElementById("num").value;
            var v3=document.getElementById("pwd").value;
            var v4=document.getElementById("cpwd").value;

            if(v1==null || v1==""){
                alert("Please enter ur name")
            }
            else if(v2.length<10){
                alert("Mobile number must be 10 digit")
            }
            else if(v3==v4){
                alert("match")
            }
                else{
                    alert("error")
                }
        }
    </script>
    <a href="c.html">reset
        password</a>
</body>
</html>
 -->




<!-- LOOPS IMPLEMENTATION
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loop Examples with User Input</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #results {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Loop Examples in JavaScript</h1>
    <label for="numberInput">Enter numbers (comma-separated):</label>
    <input type="text" id="numberInput" placeholder="1, 2, 3, 4, 5">
    <button onclick="processNumbers()">Process Numbers</button>
    <div id="results"></div>

    <script>
        function processNumbers() {
            const input = document.getElementById('numberInput').value;
            // Split input, trim whitespace, convert to numbers, and filter out NaN values
            const numbers = input.split(',')
                .map(num => parseFloat(num.trim()))
                .filter(num => !isNaN(num));

            // Check if the numbers array is empty
            if (numbers.length === 0) {
                document.getElementById('results').innerHTML = '<p>Please enter valid numbers.</p>';
                return;
            }

            let results = '';

            // For loop: Calculate squares of numbers
            results += '<h2>For Loop Results:</h2>';
            for (let i = 0; i < numbers.length; i++) {
                results += `Square of ${numbers[i]} is ${numbers[i] ** 2}<br>`;
            }

            // For...in loop: Iterate through array indices
            results += '<h2>For...In Loop Results:</h2>';
            for (let index in numbers) {
                results += `Index ${index} has value ${numbers[index]}<br>`;
            }

            // For...of loop: Iterate through values in the array
            results += '<h2>For...Of Loop Results:</h2>';
            for (let number of numbers) {
                results += `Number is ${number}<br>`;
            }

            // While loop: Calculate the sum of numbers
            results += '<h2>While Loop Results:</h2>';
            let sum = 0;
            let i = 0;
            while (i < numbers.length) {
                sum += numbers[i];
                i++;
            }
            results += `The sum of the numbers is ${sum}<br>`;

            // Display results
            document.getElementById('results').innerHTML = results;
        }
    </script>
</body>
</html>

-->







<!--KEYBOARD AND MOUSE EVENTS
<!DOCTYPE html>
<html>
<body>
<h1>HTML DOM Events</h1>
<h2>The onkeydown Event</h2>
<p>Press a key in the input field:</p>
<input type="text" onkeydown="keyDownFunction()">
<p id="keyDownDemo"></p>

<h2>The onkeypress Event</h2>
<p>A function is triggered when the user is pressing a key in the input field:</p>
<input type="text" onkeypress="keyPressFunction()">

<h2>The keyup Event</h2>
<p>A function is triggered when the user releases a key in the input field.</p>
<p>The function transforms the input field to upper case:</p>
Enter your name: <input type="text" id="fname" onkeyup="keyUpFunction()">

<H2>Mouse Events </H2> 
<h2>The onclick Event</h2>
<p>The onclick event triggers a function when an element is clicked on.</p>
<p>Click to trigger a function that will output "Hello World":</p>
<button onclick="clickFunction()">Click me</button>
<p id="clickDemo"></p>

<h2>The ondblclick Event</h2>
<p ondblclick="doubleClickFunction()">Double-click this paragraph to trigger a function.</p>
<p id="doubleClickDemo"></p>

<h2>The onmousedown Event</h2>
<p>Click the text below!</p>
<p id="mouseDownDemo" onmousedown="mouseDown()" onmouseup="mouseUp()">
The mouseDown() function sets the color of this text to red.
The mouseUp() function sets the color of this text to blue.
</p>

<h2>The onmouseover Event</h2>
<img onmouseover="bigImg(this)" onmouseout="normalImg(this)" border="0" src="C:\Users\Dattaraj Naik\Downloads\source.gif" alt="Smiley" width="32" height="32">
<p>The function bigImg() is triggered when the user moves the mouse pointer over the image.</p>
<p>The function normalImg() is triggered when the mouse pointer is moved out of the image.</p>

<script>
function keyDownFunction() {
  document.getElementById("keyDownDemo").innerHTML = "You pressed a key inside the input field";
}

function keyPressFunction() {
  alert("You pressed a key inside the input field");
}

function keyUpFunction() {
  let x = document.getElementById("fname");
  x.value = x.value.toUpperCase();
}

function clickFunction() {
  document.getElementById("clickDemo").innerHTML = "Hello World";
}

function doubleClickFunction() {
  document.getElementById("doubleClickDemo").innerHTML += "Hello World ";
}

function mouseDown() {
  document.getElementById("mouseDownDemo").style.color = "red";
}

function mouseUp() {
  document.getElementById("mouseDownDemo").style.color = "blue";
}

function bigImg(x) {
  x.style.height = "64px";
  x.style.width = "64px";
}

function normalImg(x) {
  x.style.height = "32px";
  x.style.width = "32px";
}
</script>

</body>
</html>

-->

