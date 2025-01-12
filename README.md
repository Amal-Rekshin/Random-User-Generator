# Random User Generator

## Description
This is a simple web application that generates random user details using the [Random User API](https://randomuser.me/). The application fetches user data such as name, image, gender, date of birth, age, address, phone number, email, and password and displays it in a table format.

## Features
- Fetches random user data with a single button click.
- Displays user information in a neatly formatted table.
- Error handling in case of network issues or API errors.

## How It Works
1. The application uses the "fetch" API to retrieve random user data from the Random User API.
2. Upon clicking the **Click** button, user details are displayed dynamically in the HTML content.
3. The application utilizes HTML, CSS, and JavaScript to build a simple and responsive interface.

## Technologies Used
- **HTML**: For structuring the web page.
- **CSS**: For styling the content.
- **JavaScript**: For fetching and displaying user data dynamically.

## File Structure

- index.html: Contains the HTML structure and inline CSS styles.
- Script: JavaScript code for fetching and rendering user details.

## Usage Instructions
1. Open the “index.html” file in a web browser.
2. Click the **Click** button to generate random user data.
3. View the user information displayed in the table below the button.

## Code Overview

### HTML
Defines the structure of the web application, including the button to trigger user data generation and a container to display the fetched data.
“““html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Generator</title>
</head>
<body>
    <h1>Random User Generator</h1>
    <button onclick="generator()">Click</button>
    <div id="container"></div>
</body>
</html>
“““

### CSS
Provides basic styling for the application, ensuring the layout is clean and centered.
“““css
<style>
    h4 {
        margin: 0 50px 0 0;
    }
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    button {
        width: 60px;
        height: 20px;
        border-radius: 5px;
        border: none;
        cursor: pointer;
        background-color: rgb(160, 160, 160);
    }
</style>
“““

### JavaScript
Handles the logic for fetching data from the API and updating the DOM with the user details.
“““javascript
<script>
const container = document.getElementById('container');

async function generator() {
    try {
        const response = await fetch('https://randomuser.me/api/');
        const data = await response.json();
        const user = data.results[0];

        const userName = “${user.name.title}. ${user.name.first} ${user.name.last}”;
        const userImage = user.picture.large;
        const gender = user.gender;
        const email = user.email;
        const phone = user.phone;
        const address = “${user.location.street.number} ${user.location.street.name}, ${user.location.city}, ${user.location.state}, ${user.location.country}”;
        const age = user.dob.age;
        const dob = user.dob.date;
        const password = user.login.password;

        container.innerHTML = “
        <table>
            <tr><td><h4>UserName</h4></td><td><h2>${userName}</h2></td></tr>
            <tr><td><h4>User Image</h4></td><td><img src="${userImage}" alt="User Image" /></td></tr>
            <tr><td><h4>Gender</h4></td><td><p>${gender}</p></td></tr>
            <tr><td><h4>DOB</h4></td><td><p>${dob}</p></td></tr>
            <tr><td><h4>Age</h4></td><td><h3>Age: ${age}</h3></td></tr>
            <tr><td><h4>Address</h4></td><td><p>${address}</p></td></tr>
            <tr><td><h4>Phone No.</h4></td><td><h5>${phone}</h5></td></tr>
            <tr><td><h4>E-Mail</h4></td><td><p>${email}</p></td></tr>
            <tr><td><h4>Password</h4></td><td><p>${password}</p></td></tr>
        </table>“;
    } catch (err) {
        container.textContent = "Error found: " + err.message;
    }
}
</script>
“““

## Demo
1. Open the application in any modern web browser.
2. Click the **Click** button to fetch and display a random user's details.

## Error Handling
- If an error occurs during the API call, the application will display an error message inside the container.

## Dependencies
- [Random User API](https://randomuser.me/) for fetching user data.

## Screenshots
![Application Screenshot](#)

## License
This project is open-source and available under the MIT License.

