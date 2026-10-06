<!DOCTYPE html>
<html>
<head>
    <title>Grade Calculator</title>

    <style>
        body {
            font-family: Arial;
            background-color: #f2f2f2;
            text-align: center;
            padding: 40px;
        }

        .box {
            background: white;
            width: 350px;
            margin: auto;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }

        input {
            width: 90%;
            padding: 10px;
            margin: 8px;
            border: 1px solid gray;
            border-radius: 5px;
        }

        button {
            background-color: blue;
            color: white;
            border: none;
            padding: 10px 25px;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: darkblue;
        }

        #result {
            margin-top: 20px;
            font-size: 18px;
            color: green;
        }
    </style>
</head>

<body>

<div class="box">

    <h2>Student Grade Calculator</h2>

    <input type="number" id="m1" placeholder="Subject 1 Marks">
    <input type="number" id="m2" placeholder="Subject 2 Marks">
    <input type="number" id="m3" placeholder="Subject 3 Marks">
    <input type="number" id="m4" placeholder="Subject 4 Marks">
    <input type="number" id="m5" placeholder="Subject 5 Marks">

    <br>

    <button onclick="calculate()">Calculate</button>

    <div id="result"></div>

</div>

<script>

function calculate() {

    let a = Number(document.getElementById("m1").value);
    let b = Number(document.getElementById("m2").value);
    let c = Number(document.getElementById("m3").value);
    let d = Number(document.getElementById("m4").value);
    let e = Number(document.getElementById("m5").value);

    let total = a + b + c + d + e;
    let percentage = total / 5;

    let grade;

    if (percentage >= 90)
        grade = "A+";
    else if (percentage >= 80)
        grade = "A";
    else if (percentage >= 70)
        grade = "B";
    else if (percentage >= 60)
        grade = "C";
    else if (percentage >= 50)
        grade = "D";
    else
        grade = "F";

    document.getElementById("result").innerHTML =
        "Total: " + total + "/500<br>" +
        "Percentage: " + percentage + "%<br>" +
        "Grade: " + grade;
}

</script>

</body>
</html>
