# 🔐 Custom Password Generator

A sleek, robust, and highly responsive web application engineered to generate cryptographically secure passwords with real-time strength analysis.

* **Live Demo Link:** https://sk-reyad.github.io/Password-Generator/

---

# 📝 Project Overview

This is a client-side utility designed with a strict focus on modern UI/UX principles and digital security. It provides users with complete control over their password complexity through an intuitive, interactive interface. Unlike basic random string generators, this application features a sophisticated, algorithm-driven strength meter that evaluates character diversity and length in real-time, providing immediate visual feedback. 

From quick 6-character PINs to uncrackable 24-character security keys, this tool ensures users generate robust credentials effortlessly, complete with a seamless one-click copy experience.

---

# ✨ Key Features

* **Granular Complexity Control:** Toggle specific character sets including Uppercase, Lowercase, Numbers, and Symbols to meet strict password requirements.
* **Dynamic Range Slider:** Smooth, responsive length adjustment (from 6 to 24 characters) that updates the password generation engine instantly on user input.
* **Real-Time Strength Analytics:** A dynamic, color-coded strength bar (Weak, Medium, Strong) that calculates password entropy on the fly based on length and character combinations.
* **Smart Clipboard Integration:** One-click copy functionality featuring custom UI feedback—the copy icon instantly morphs into a green success checkmark to confirm action completion.
* **Zero-State Prevention:** Auto-generates a secure password immediately upon page load so the user is never met with an empty field.
* **Fluid Responsiveness:** Perfectly scales down to 400px viewports, ensuring a seamless experience across desktop, tablet, and mobile devices.

---

# 🧠 Technical Highlights (Skills Showcase)

This project was built from scratch without reliance on external UI frameworks, demonstrating a deep, applied understanding of modern web development:

### Advanced JavaScript Logic & DOM Manipulation
* **Algorithmic Strength Calculation:** Rather than relying on basic string length, the `updateStrength` function utilizes Regular Expressions (Regex) (e.g., `/[A-Z]/`, `/[!@#$%...]/`) to verify character diversity. It computes a weighted score (scaling up to 100) to dynamically adjust the DOM's CSS width and color variables for the strength meter.
* **Asynchronous Clipboard API:** Implemented modern browser APIs (`navigator.clipboard.writeText`) using a Promise chain (`.then().catch()`). Coupled with `setTimeout`, it orchestrates a smooth, temporary UI state change for user feedback by dynamically toggling FontAwesome classes (`fa-copy` to `fa-check`).
* **Event-Driven Architecture:** Leverages precise event listeners (`input` for continuous slider updates, `click` for generation/copying, and `DOMContentLoaded` for initialization) to maintain a highly reactive interface.

### Modern CSS3 Architecture & Styling
* **Custom Properties (Variables):** Utilized `:root` variables to establish a centralized design system. This allows for semantic color management (`--primary-color`, `--strong-color`) and makes future theme adaptations effortless.
* **Flexbox Mastery:** Extensively applied Flexbox properties (`justify-content: space-between`, `gap`, `flex-shrink`) to construct a resilient layout that prevents text overflow and maintains perfect alignment across the options panel and control bar.
* **Custom Input Styling:** Completely overhauled native browser inputs. I stripped default styles from `input[type="checkbox"]` using `appearance: none` and rebuilt them with custom borders, transitions, and `::after` pseudo-elements to render a bespoke checkmark.

### Semantic HTML5 & Accessibility
* **Accessible Structure:** Implemented clear `<label>` associations for all inputs to ensure screen reader compatibility and improve click targets.
* **Input Protection:** Strategically utilized the `readonly` attribute on the primary password `<input>`, preventing accidental user keystrokes while keeping the generated string selectable for the Clipboard API.

---

# 🛠️ Tech Stack

* **HTML5:** Semantic architecture and accessible forms.
* **CSS3:** Custom Variables, Flexbox, Pseudo-elements, and Media Queries.
* **JavaScript (ES6+):** Modular functions, DOM API, Regex, and Promises.
* **FontAwesome (6.5.1):** Scalable vector icons.
* **Google Fonts:** Montserrat typeface for a clean, modern aesthetic.

---

# 🚀 Quick Start

* **Clone the repository:**
```bash
git clone https://github.com/sk-reyad/password-generator.git
```

* **Navigate to the project directory:**
```bash
cd password-generator
```

* **Run the application:**
Simply open the `index.html` file in your preferred web browser. No local server or build tools required!

---

# 📬 Let's Connect
* 📧 **Email:** skreyad2016@gmail.com
* 💼 **LinkedIn:** [https://www.linkedin.com/in/sk-reyad/](https://www.linkedin.com/in/sk-reyad/)
