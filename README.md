### STANDARD CALCULATOR USING JAVASCRIPT:

### HTML:
```
<!DOCTYPE html>
<html lang="en">
    <link rel="stylesheet" href="style.css">
<head>
    <title>JavaScript Calculator</title>
<body>
<div class="formstyle">
    <form name="form1">
        <input id="calc" type="text" name="answer"><br><br>
        <input type="button" value="1" onclick="addToExpression('1')">
        <input type="button" value="2" onclick="addToExpression('2')">
        <input type="button" value="3" onclick="addToExpression('3')">
        <input type="button" value="+" onclick="addToExpression('+')"><br><br>
        <input type="button" value="4" onclick="addToExpression('4')">
        <input type="button" value="5" onclick="addToExpression('5')">
        <input type="button" value="6" onclick="addToExpression('6')">
        <input type="button" value="-" onclick="addToExpression('-')"><br><br>
        <input type="button" value="7" onclick="addToExpression('7')">
        <input type="button" value="8" onclick="addToExpression('8')">
        <input type="button" value="9" onclick="addToExpression('9')">
        <input type="button" value="" onclick="addToExpression('')"><br><br>
        <input type="button" value="/" onclick="addToExpression('/')">
        <input type="button" value="0" onclick="addToExpression('0')">
        <input type="button" value="." onclick="addToExpression('.')">
        <input type="button" value="=" onclick="calculateResult()"><br>
        <input type="button" value="C" onclick="clearExpression()">
        <input type="button" value="Clear All" onclick="clearExpression()" id="clear"><br>
    </form>
    <script src="script.js"></script>
</div>
</body>
</html>
```
### CSS:
```
h1 {
    text-align: center;
    padding: 23px;
    background-color: skyblue;
    color: white;
}

#clear {
    width: 270px;
    border: 3px solid gray;
    border-radius: 3px;
    padding: 20px;
    background-color: rgb(154, 12, 36);
}

.formstyle {
    width: 300px;
    height: 570px;
    margin: auto;
    border: 3px solid skyblue;
    border-radius: 5px;
    padding: 20px;
}

input {
    width: 10px;
    background-color: rgb(0, 128, 109);
    color: white;
    border: 3px solid gray;
    border-radius: 10px;
    padding: 26px;
    margin: 5px;
    font-size: 10px;
    height: 50px;
}

#calc {
    width: 250px;
    border: 5px solid black;
    border-radius: 3px;
    padding: 20px;
    margin: auto;
}
```
### JAVASCRIPT:
```
function addToExpression(value) {
    document.form1.answer.value += value;
}

function calculateResult() {
    try {
        document.form1.answer.value = eval(document.form1.answer.value);
    } catch (e) {
        document.form1.answer.value = 'Error';
    }
}

function clearExpression() {
    document.form1.answer.value = '';
}
function handlekeyup(form1) {
    const allowedKeys = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '+', '-', '*', '/', '.','C'];
    const key = key;
    if (key === 'Enter') {
        calculateResult();
    } else if (allowedKeys.includes(key)) {
        document.form1.answer.value += key;
    } else if (key === 'Backspace' || key === 'Delete') {
        document.form1.answer.value = document.form1.answer.value.slice(0, -1);
    }
}
```
### OUTPUT:
![Screenshot (4)](https://github.com/akasharuna003/standard-calculator/assets/135735278/ace2cc7c-210d-4932-9a90-28b8ecc3ee34)
