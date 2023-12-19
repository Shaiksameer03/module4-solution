<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Names Greeting</title>
    <!-- Linking jQuery -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <!-- Linking Lodash -->
    <script src="https://cdn.jsdelivr.net/npm/lodash@4.17.21/lodash.min.js"></script>
</head>
<body>
    <!-- Your HTML content here -->
    <h1>Greetings</h1>
    <ul id="greetings-list"></ul>

    <!-- JavaScript code -->
    <script>
        // Array of names
        const names = ['Bobby', 'Jaanu', 'Sweety', 'Mary', 'Jasmine'];

        // Loop through the array using lodash and create greetings
        _.forEach(names, name => {
            // Check if the name starts with 'j' or 'J' using jQuery
            if ($.trim(name).charAt(0).toLowerCase() === 'j') {
                // Print Goodbye to console and create list item
                console.log(`Goodbye ${name}`);
                $('#greetings-list').append(`<li>Goodbye ${name}</li>`);
            } else {
                // Print Hello to console and create list item
                console.log(`Hello ${name}`);
                $('#greetings-list').append(`<li>Hello ${name}</li>`);
            }
        });
    </script>
</body>
</html>
