<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Search Bar with Toggle Buttons</title>
    <style>
        .toggle-buttons {
            display: inline-block;
        }
        
        .toggle-buttons button {
            background-color: #ccc;
            border: none;
            color: black;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 4px;
        }
        
        .toggle-buttons button.active {
            background-color: #007bff;
            color: white;
        }
    </style>
</head>
<body>
    <form action="#" method="get" onsubmit="return checkButton()">
        <input type="text" name="search" id="search" style="width: 400px;" placeholder="Enter your search term">
        <button type="submit">Search</button>
        <div class="toggle-buttons">
            <button id="publicBtn" type="button" onclick="toggleButtons('publicBtn')">Public</button>
            <button id="privateBtn" type="button" onclick="toggleButtons('privateBtn')">Private</button>
        </div>
    </form>
    <script>
        var ian;

        function toggleButtons(activeButtonId) {
            var buttons = document.querySelectorAll('.toggle-buttons button');
            buttons.forEach(function(button) {
                if (button.id === activeButtonId) {
                    button.classList.add('active');
                } else {
                    button.classList.remove('active');
                }
            });
        }

        function checkButton() {
            var publicBtn = document.getElementById('publicBtn');
            var isPublicActive = publicBtn.classList.contains('active');
            if (isPublicActive) {
                alert('Public button is active!');
                ian = "public";
            } else {
                alert('Private button is active!');
                ian = "private";
            }
            console.log(ian); // just for testing purposes
            return false; // Prevent form submission for demonstration purposes
        }

        document.getElementById('search').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                checkButton();
            }
        });
    </script>
</body>
</html>
