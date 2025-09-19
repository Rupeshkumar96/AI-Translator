# AI-Translator
AI Translator automatically detects the source language of text input and translates it instantly into multiple target languages with high accuracy.

# 🤖 Real-Time AI Text Translator

<p align="center">
    <a href="#"><img src="https://img.shields.io/badge/Language-JavaScript-yellow?style=for-the-badge&logo=javascript"></a>
    <a href="#"><img src="https://img.shields.io/badge/Styling-CSS-blue?style=for-the-badge&logo=css3"></a>
    <a href="#"><img src="https://img.shields.io/badge/API-Google_Translate_v2-red?style=for-the-badge&logo=google"></a>
    <a href="#"><img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"></a>
</p>

## ✨ Overview

The **Real-Time AI Text Translator** is a sleek, modern, single-page web application that provides instant, high-quality language detection and translation. Built purely with **HTML, CSS, and vanilla JavaScript**, it leverages the powerful **Google Cloud Translation API (v2)** to process and translate text across multiple languages as you type.

This project is ideal for developers looking for a clean, front-end example of consuming a major commercial translation API, or for anyone needing a fast, efficient, and visually appealing translation tool.

---

## 🚀 Features

The application is designed for simplicity and speed, offering the following core functionalities:

| Feature | Description | Implementation Detail |
| :--- | :--- | :--- |
| **Real-Time Translation** | Automatically translates text as the user types, thanks to a built-in **debounce mechanism** that limits API calls. | `translateText()` function with `debounce()`. |
| **Automatic Language Detection** | Detects the source language of the input text, displaying the language name and a confidence score. | `detectLanguage()` function via Google API. |
| **Multi-Language Support** | Supports translation to a pre-defined list of popular world languages via a clean dropdown selector. | Utilizes Google Translation API's extensive language capabilities. |
| **Text-to-Speech (TTS)** | Allows users to listen to the translated text for pronunciation verification and accessibility. | Native Web Speech API (`SpeechSynthesisUtterance`). |
| **Utility Controls** | Quick actions for **Clearing** the input and **Copying** the translated output to the clipboard. | Standard JavaScript DOM manipulation and `navigator.clipboard.writeText()`. |
| **Keyboard Shortcuts** | Productivity enhancements for power users: `Ctrl/Cmd + Enter` to translate, `Ctrl/Cmd + D` to detect language, and `Ctrl/Cmd + K` to clear. | Event listener on `keydown`. |

---

## 🛠️ Installation and Setup

This project is a standalone web application. No server-side installation is required, but you **must** obtain and configure an API key for the translation service to function.

### 1. API Key Configuration

1.  Get a **Google Cloud Translation API (v2)** key from the Google Cloud Console. *Note: The API is a paid service, and you may need to enable billing.*
2.  In the `index.html` file (or your main HTML file), locate the following line within the `<script>` tag:

    ```javascript
    this.apiKey = 'AIzaSyCQzfkar_FaUictSktha13dFXeHibl1ldw'; // <-- REPLACE THIS
    ```

3.  Replace the placeholder value with your actual Google Translation API key.

### 2. Running the Application

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/real-time-ai-translator.git](https://github.com/your-username/real-time-ai-translator.git)
    cd real-time-ai-translator
    ```
2.  **Open the file:** Simply open the `index.html` file in your preferred web browser.

    ```bash
    # Command line (for Linux/macOS users):
    open index.html
    ```

---

## ⚙️ Project Structure & Technology

The entire application is contained within a single `index.html` file, demonstrating efficient encapsulation of logic and styling.

### Technologies Used

* **HTML5:** Structure and content.
* **CSS3:** Styling, using a modern, responsive design with a gradient background and **Inter** font.
* **Vanilla JavaScript (ES6+):** All application logic, including API handling, DOM manipulation, and utility functions like `debounce`.
* **Google Cloud Translation API (v2):** The core backend service for language detection and translation.
* **Font Awesome:** Used for icons to enhance the user interface (`fas fa-language`, `fas fa-exchange-alt`, etc.).

### Key JavaScript Concepts

The main application logic is managed by the `Translator` class, which handles all user interactions and API communication.

* **`debounce(func, wait)`:** A crucial utility function that ensures the `translateText` function is not called too frequently (e.g., on every single keystroke), thus preventing unnecessary strain on the API quota and improving performance.
* **`async/await` and `fetch`:** Used for making asynchronous, modern HTTP requests to the Google Translation API endpoints (`/v2` and `/v2/detect`).
* **Web Speech API (`SpeechSynthesisUtterance`):** Provides the client-side capability to read the translated text aloud.

---

## 🤝 Contribution

Contributions are welcome! If you have suggestions for new features, bug fixes, or improvements to the styling, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
