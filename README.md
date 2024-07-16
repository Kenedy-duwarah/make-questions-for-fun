<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Question Generating </title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        h1 {
            margin-bottom: 20px;
        }
        
        form {
            margin-bottom: 20px;
        }
        
        input[type="text"] {
            width: calc(100% - 22px);
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            background-color: #007BFF;
            color: #fff;
            border-radius: 4px;
            cursor: pointer;
        }
        
        button:hover {
            background-color: #0056b3;
        }
        
        #generatedQuestion {
            margin-top: 20px;
            font-size: 1.2em;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1>Question Generate 😄</h1>
        <form id="questionForm">
            <label for="questionInput">Enter your question:</label>
            <input type="text" id="questionInput" required>
            <button type="submit">Generate Question</button>
        </form>
        <div id="generatedQuestion"></div>
    </div>
    <script>
        document.getElementById('questionForm').addEventListener('submit', function(event) {
            event.preventDefault();

            const questionInput = document.getElementById('questionInput').value;

            // Simulate API call
            generateQuestion(questionInput);
        });

        function generateQuestion(input) {
            // Simulating a response from an API
            const generatedResponse = `Generated question based on your input: ${input}?`;

            document.getElementById('generatedQuestion').textContent = generatedResponse;
        }
    </script>
</body>

</html>
