# Random User Generator

## Overview
This project is a simple web application that generates random user information using the [Random User API](https://randomuser.me/). It fetches data like the user's name, image, gender, date of birth, age, address, phone number, email, and password and displays it in a clean and organized format.

## Features
- Fetches random user data from the Random User API.
- Displays user details dynamically in an HTML table.
- Simple and clean user interface.
- Handles errors gracefully with user-friendly messages.

## Live Demo
You can try the application live at [Random User Generator Demo](#). *(`https://amal-rekshin.github.io/Random-User-Generator/`)*

## Getting Started

### Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge).
- Internet connection to fetch data from the API.

### Usage
1. Open the application in your browser.
2. Click the **Click** button to fetch random user details.
3. The fetched data will be displayed in a table below the button.

## Technologies Used
- **HTML**: To structure the content.
- **CSS**: For basic styling and layout.
- **JavaScript**: To fetch and display data dynamically from the API.

## File Structure
```
random-user-generator/
├── index.html   # Main HTML file
└── README.md    # Documentation
```

## Example Output
A random user detail will look like this:

| Field       | Value                          |
|-------------|--------------------------------|
| User Name   | Mr. John Doe                  |
| User Image  | ![User Image](user_image_url) |
| Gender      | Male                          |
| Date of Birth | 1990-05-15                   |
| Age         | 33                            |
| Address     | 123 Elm St, Springfield, USA |
| Phone       | +1-555-555-5555              |
| Email       | johndoe@example.com          |
| Password    | secretpassword123            |

## Error Handling
If the API request fails, an error message will be displayed in place of the user details.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
- Thanks to [Random User API](https://randomuser.me/) for providing the user data.

