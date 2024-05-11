# Ex.08 Design of a Standard Calculator
## NAME:DILLIARASU.M
## RIGISTER NUMBER:212223230049
## Date:

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
## calc.html:
```
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Calculator</h1>
        <h3 class="text">DILLIARASU M (212223230049)</h3>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color">C</button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button class="color">*</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button class="color">-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button class="color">+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button class="color">.</button></td>
                    <td><button class="color">/</button></td>
                    <td><button class="color">=</button></td>
                </tr>
            </table>
        </div>
    </div>

    <script src="calc.js"></script>
</body>
</html>
```
## styles.css
```
.container {
    text-align: center;
    margin-top: 23px;
}

.calculator {
    border: none;
    background-color: #f6fa83;
    padding: 30px;
    border-radius: 30px;
    display: inline-block;
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

h3 {
    font-size: 20px;
    font-weight: bold;
    color: black;
    text-align: center;
    margin: auto;
    margin-top: 20px;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(45, 129, 129);
    padding: 20px;
    background: rgb(255, 255, 255);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border-radius: 20px;
    border: 0;
    outline: 0;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: transparent;
    color: rgb(11, 11, 11);
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.color {
    color: rgb(97, 142, 248);
}
```
## calc.js:
```
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```
## OUTPUT:

![WhatsApp Image 2024-05-11 at 21 27 17_f406e586](https://github.com/Dilliarasu0105/Calc/assets/144979593/00549752-dcab-4b13-915e-bf4b8b92d776)

![WhatsApp Image 2024-05-11 at 21 27 18_4f22c9d0](https://github.com/Dilliarasu0105/Calc/assets/144979593/1f3328d4-b93f-4827-b963-bc06afdc6944)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
