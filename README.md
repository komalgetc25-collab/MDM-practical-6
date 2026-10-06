<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Student Grade Calculator</title>

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
</head>

<body class="bg-gray-100">

  <div class="max-w-md mx-auto mt-10 bg-white p-6 rounded-lg shadow-lg">

    <h1 class="text-2xl font-bold text-center text-blue-600 mb-6">
      Student Grade Calculator
    </h1>

    <!-- Marks Input -->
    <label class="block mb-2 font-semibold">
      Enter marks for 5 subjects
    </label>

    <input id="mark1" type="number" placeholder="Subject 1"
      class="w-full border p-2 rounded mb-3">

    <input id="mark2" type="number" placeholder="Subject 2"
      class="w-full border p-2 rounded mb-3">

    <input id="mark3" type="number" placeholder="Subject 3"
      class="w-full border p-2 rounded mb-3">

    <input id="mark4" type="number" placeholder="Subject 4"
      class="w-full border p-2 rounded mb-3">

    <input id="mark5" type="number" placeholder="Subject 5"
      class="w-full border p-2 rounded mb-4">

    <!-- Calculate Button -->
    <button onclick="calculateGrade()"
      class="w-full bg-blue-600 text-white py-2 rounded
             hover:bg-blue-700">
      Calculate Grade
    </button>

    <!-- Result -->
    <div id="result"
      class="mt-6 text-center font-semibold text-lg">
    </div>

  </div>


  <script>

    function calculateGrade() {

      // Get marks
      let m1 = Number(document.getElementById("mark1").value);
      let m2 = Number(document.getElementById("mark2").value);
      let m3 = Number(document.getElementById("mark3").value);
      let m4 = Number(document.getElementById("mark4").value);
      let m5 = Number(document.getElementById("mark5").value);

      // Calculate total
      let total = m1 + m2 + m3 + m4 + m5;

      // Calculate percentage
      let percentage = total / 5;

      // Calculate grade
      let grade;

      if (percentage >= 90) {
        grade = "A+";
      }
      else if (percentage >= 80) {
        grade = "A";
      }
      else if (percentage >= 70) {
        grade = "B";
      }
      else if (percentage >= 60) {
        grade = "C";
      }
      else if (percentage >= 50) {
        grade = "D";
      }
      else {
        grade = "F";
      }

      // Display result
      document.getElementById("result").innerHTML =
        "Total Marks: " + total + " / 500<br>" +
        "Percentage: " + percentage.toFixed(2) + "%<br>" +
        "Grade: " + grade;
    }

  </script>

</body>
</html>
