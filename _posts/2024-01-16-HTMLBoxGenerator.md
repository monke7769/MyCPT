<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Button Generator</title>
    <style>
        #button-container {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <form id="htmlForm">
        <label for="htmlInput">HTML Input:</label>
        <input type="text" id="htmlInput" name="htmlInput" required>
        
        <input type="button" value="Generate Button" onclick="generateButton()">
    </form>

    <div id="button-container"></div>

    <script>
        function generateButton() {
            const htmlInputValue = document.getElementById('htmlInput').value;
            const buttonContainer = document.getElementById('button-container');
            
            // Create a div element to hold the button
            const buttonWrapper = document.createElement('div');
            
            // Set the innerHTML of the div with the HTML input value
            buttonWrapper.innerHTML = htmlInputValue;
            
            // Append the div to the button container
            buttonContainer.innerHTML = ''; // Clear previous content
            buttonContainer.appendChild(buttonWrapper);
        }
    </script>

</body>
</html>