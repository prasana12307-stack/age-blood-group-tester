# age-blood-group-tester
<!DOCTYPE html>
<html>
<head>
    <title>Person Eligibility Checker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            text-align: center;
            padding: 30px;
        }

        .container {
            background: white;
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }

        input, select {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
        }

        button {
            background-color: blue;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
        }

        #result {
            margin-top: 20px;
            text-align: left;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Person Information Checker</h2>

    <label>Blood Group:</label>
    <select id="bloodGroup">
        <option>A+</option>
        <option>A-</option>
        <option>B+</option>
        <option>B-</option>
        <option>AB+</option>
        <option>AB-</option>
        <option>O+</option>
        <option>O-</option>
    </select>

    <label>Age:</label>
    <input type="number" id="age" placeholder="Enter your age">

    <label>Favorite Color:</label>
    <input type="text" id="color" placeholder="Enter favorite color">

    <button onclick="checkInfo()">Check</button>

    <div id="result"></div>
</div>

<script>
function checkInfo() {
    let bloodGroup = document.getElementById("bloodGroup").value;
    let age = parseInt(document.getElementById("age").value);
    let color = document.getElementById("color").value;

    let voteStatus = age >= 18
        ? "✅ Eligible to Vote"
        : "❌ Not Eligible to Vote";

    document.getElementById("result").innerHTML = `
        <h3>Results</h3>
        <p><strong>Blood Group:</strong> ${bloodGroup}</p>
        <p><strong>Age:</strong> ${age}</p>
        <p><strong>Favorite Color:</strong> ${color}</p>
        <p><strong>Voting Status:</strong> ${voteStatus}</p>
    `;
}
</script>

</body>
</html>
