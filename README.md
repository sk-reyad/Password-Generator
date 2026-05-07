# Custom Password Generator

A sleek, responsive, and interactive password generator built with **HTML**, **CSS**, and **JavaScript**. This project allows users to generate random passwords based on selected character types, customize password length, view password strength instantly, and copy the generated password with one click.

**Live Demo:** [https://password-generator-two-lilac.vercel.app/](https://password-generator-two-lilac.vercel.app/)

**Source Code:** [https://github.com/sk-reyad/Password-Generator](https://github.com/sk-reyad/Password-Generator)

**Alternative Demo:** [https://sk-reyad.github.io/Password-Generator/](https://sk-reyad.github.io/Password-Generator/)

---

## Overview

The **Custom Password Generator** is a client-side web application designed to make password creation simple, fast, and visually engaging. Users can control password complexity by selecting character types such as uppercase letters, lowercase letters, numbers, and symbols. The application then generates a random password based on those selected options.

The project focuses on both practical functionality and clean user experience. It includes a modern card-based interface, responsive layout, custom form controls, a real-time password strength indicator, and clipboard support for quick copying. This makes the project a strong frontend practice project that demonstrates DOM manipulation, event handling, JavaScript logic, responsive styling, and user-focused interface design.

---

## Features

* Generate random passwords instantly in the browser
* Select password length from **6 to 24 characters**
* Include or exclude:

  * Uppercase letters
  * Lowercase letters
  * Numbers
  * Symbols
* Live password length display while using the range slider
* Real-time password strength analysis
* Password strength shown as:

  * Weak
  * Medium
  * Strong
* Color-coded strength bar for better visual feedback
* One-click copy-to-clipboard feature
* Copy icon changes into a success checkmark after copying
* Automatically generates a password when the page loads
* Shows an alert if no character type is selected
* Responsive design for desktop, tablet, and mobile screens
* Modern gradient background with a clean white generator card
* Custom checkbox styling for a polished interface
* Uses Font Awesome icons for a better visual experience

---

## Technologies Used

* **HTML5** — for the main structure, input fields, labels, and layout
* **CSS3** — for styling, responsive design, custom variables, Flexbox, gradients, transitions, and custom checkboxes
* **JavaScript** — for password generation, DOM updates, event handling, strength checking, and clipboard functionality
* **Font Awesome 6.5.1** — for the copy, check, and key icons
* **Google Fonts** — for the Montserrat font used in the interface

---

## What I Learned

Through this project, I practiced building a fully interactive frontend application using only HTML, CSS, and JavaScript.

I learned how to connect user input controls with JavaScript logic. The password length slider updates the selected length immediately, which helped me understand how real-time UI updates work using event listeners.

I also practiced conditional logic by checking which character options the user selected. Based on those selections, the JavaScript creates a combined character pool and generates a password by randomly selecting characters from that pool.

Another important part of this project was the password strength system. I used password length and character variety to calculate strength and update the UI dynamically. This helped me understand how logic and visual feedback can work together to improve user experience.

I also worked with the Clipboard API to copy the generated password directly from the browser. The temporary icon change after copying helped me practice giving users clear interaction feedback.

On the CSS side, I improved my understanding of responsive layouts, Flexbox, CSS variables, custom input styling, gradients, shadows, transitions, and media queries. Overall, this project helped me strengthen both JavaScript functionality and frontend presentation skills.

---

## Project Structure

```text
Password-Generator/
│
├── assets/
│   └── logo.svg
│
├── index.html
├── style.css
├── script.js
└── README.md
```

### `index.html`

This file contains the main structure of the password generator. It includes the password display field, copy button, length slider, checkbox options, generate button, and password strength section.

### `style.css`

This file handles the complete visual design of the project. It includes the gradient background, generator card, custom checkboxes, buttons, password field, strength bar, responsive layout, and mobile-friendly adjustments.

### `script.js`

This file contains the main functionality of the application. It manages password generation, selected character options, slider updates, strength checking, copy-to-clipboard behavior, and automatic password generation on page load.

### `assets/logo.svg`

This file stores the project logo or favicon used in the browser tab.

---

## How It Works

When the website loads, the JavaScript file automatically generates an initial password so the user immediately sees a result.

The user can then adjust the password length using the range slider. The selected length updates live beside the slider. The user can also select which character types should be included in the password.

When the **Generate Password** button is clicked, the script checks the selected options. If no option is selected, it shows an alert asking the user to select at least one character type. If one or more options are selected, the script combines the selected character groups into one character pool.

After that, JavaScript creates the password by repeatedly selecting random characters from the combined pool until the password reaches the selected length. The generated password is then displayed inside the readonly password field.

The password strength checker analyzes the generated password based on length and character variety. It updates the strength label and adjusts the strength bar to show whether the password is weak, medium, or strong.

The copy button uses the browser Clipboard API to copy the generated password. After copying, the icon temporarily changes into a checkmark to confirm the action.

---

## Password Strength Logic

The strength meter is based on a simple scoring approach. The password becomes stronger when it has a longer length and contains a wider variety of character types.

The strength checker considers:

* Password length
* Uppercase letters
* Lowercase letters
* Numbers
* Symbols

The final result is shown visually:

```text
Weak   → Red strength bar
Medium → Yellow strength bar
Strong → Green strength bar
```

This gives users quick and clear feedback about the quality of the generated password.

---

## UI/UX Highlights

The design is focused on clarity, simplicity, and smooth interaction.

Key design details include:

* Clean centered layout
* Modern gradient background
* White card-style password generator box
* Rounded corners and soft shadow
* Readonly password field to prevent accidental editing
* Circular copy button with icon feedback
* Custom-designed checkboxes
* Smooth hover effect on the generate button
* Responsive layout for smaller devices
* Clear visual password strength indicator

---

## Setup and Usage

### 1. Clone the Repository

```bash
git clone https://github.com/sk-reyad/Password-Generator.git
```

### 2. Navigate to the Project Folder

```bash
cd Password-Generator
```

### 3. Open the Project

Open the `index.html` file in any modern web browser.

No installation, package manager, build tool, or local server is required.

---

## Deployment

This project can be deployed easily using static hosting platforms because it only uses HTML, CSS, and JavaScript.

Current deployment links:

* **Vercel Live Demo:** [https://password-generator-two-lilac.vercel.app/](https://password-generator-two-lilac.vercel.app/)
* **GitHub Pages Demo:** [https://sk-reyad.github.io/Password-Generator/](https://sk-reyad.github.io/Password-Generator/)
* **GitHub Repository:** [https://github.com/sk-reyad/Password-Generator](https://github.com/sk-reyad/Password-Generator)

---

## Browser Support

This project works best in modern browsers such as:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

The copy feature depends on the browser’s Clipboard API, so it works best in browsers that support `navigator.clipboard`.

---

## Security Note

This project is a frontend learning project and uses JavaScript-based random password generation. It is suitable for demonstrating password generation logic, UI interaction, DOM manipulation, and frontend development skills.

For a more security-focused production version, the password generation logic could be improved by using the Web Crypto API, such as `crypto.getRandomValues()`, for stronger randomness.

---

## Future Improvements

Possible future improvements include:

* Use `crypto.getRandomValues()` for stronger random password generation
* Ensure at least one character from each selected character type appears in the generated password
* Add a password visibility toggle
* Add an option to exclude similar-looking characters such as `O`, `0`, `l`, and `1`
* Add a password history section for recently generated passwords
* Add dark mode support
* Add a copy success toast message
* Add more detailed password strength feedback
* Add an option to generate memorable passphrases
* Improve accessibility with more ARIA labels and keyboard focus states

---

## Author

**SK Reyad Ali**

---

## Contact

* Email: [skreyad2016@gmail.com](mailto:skreyad2016@gmail.com)
* LinkedIn: [https://www.linkedin.com/in/sk-reyad/](https://www.linkedin.com/in/sk-reyad/)
