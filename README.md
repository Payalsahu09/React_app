🔐 React Password Generator

A simple yet powerful Password Generator App built using React.js.
This project allows users to generate secure, customizable passwords instantly, with options to include uppercase letters, lowercase letters, numbers, and symbols.

✨ Features

✅ Generate random passwords instantly
✅ Choose password length (from 6–30 characters)
✅ Toggle character types (uppercase, lowercase, numbers, symbols)
✅ Copy password to clipboard with one click
✅ Responsive design — works on all devices
✅ Clean, minimal UI built with TailwindCSS

🧩 Tech Stack

Frontend: React.js (with Vite or Create React App)

Styling: TailwindCSS (or plain CSS)

Icons: React Icons / Feather Icons

Clipboard API: For copy-to-clipboard functionality

🚀 Getting Started
1️⃣ Clone the repository
git clone https://github.com/your-username/react-password-generator.git
cd react-password-generator

2️⃣ Install dependencies
npm install
# or
yarn install

3️⃣ Start the development server
npm run dev
# or
yarn dev

4️⃣ Open in browser

Visit: http://localhost:5173
 (if using Vite)
or http://localhost:3000
 (if using Create React App)

🧠 How It Works

The user selects the password length using a slider or number input.

Toggles different options (uppercase, lowercase, numbers, symbols).

Clicks Generate Password.

The app creates a random combination using JavaScript’s Math.random() and string character sets.

The generated password is displayed, with a Copy button to copy it to clipboard.

Example password logic:

const chars = {
  upper: "ABCDEFGHIJKLMNOPQRSTUVWXYZ",
  lower: "abcdefghijklmnopqrstuvwxyz",
  numbers: "0123456789",
  symbols: "!@#$%^&*()_+{}[]<>?/",
};

const generatePassword = (length, options) => {
  let validChars = "";
  if (options.upper) validChars += chars.upper;
  if (options.lower) validChars += chars.lower;
  if (options.numbers) validChars += chars.numbers;
  if (options.symbols) validChars += chars.symbols;

  let password = "";
  for (let i = 0; i < length; i++) {
    password += validChars.charAt(Math.floor(Math.random() * validChars.length));
  }
  return password;
};

📁 Folder Structure
react-password-generator/
├── public/
│   └── index.html
├── src/
│   ├── App.jsx
│   ├── components/
│   │   └── PasswordGenerator.jsx
│   ├── styles/
│   │   └── index.css
│   └── main.jsx
└── README.md

💡 Example UI Flow

1️⃣ User chooses:

Length: 12

Include: ✅ Uppercase ✅ Numbers ❌ Symbols

2️⃣ Clicks “Generate Password”

🧩 Output:

Q8jD2hKxR7sT


3️⃣ Clicks “Copy” → Password copied to clipboard ✅

📱 Responsive Design

Mobile-friendly (100% width inputs/buttons)

Centered layout using Tailwind’s flex utilities

Smooth color transitions and hover effects

⚙️ Customization

You can easily extend this project:

Add password strength indicator

Add dark/light mode

Add auto-copy notification (e.g., “Copied!” toast)

Add generate multiple passwords option

Save passwords to localStorage

🧾 License

This project is licensed under the MIT License — feel free to use and modify it.
