# Password Generator Flask

🔐 A modern, feature-rich password generator web application built with Flask.

## Overview

Password Generator Flask is a sleek and intuitive web application that creates strong, secure passwords with customizable options. It features a beautiful dark-themed interface with real-time password strength visualization.

## Features

✨ **Modern Dark UI** - Clean, contemporary design with smooth animations

🔠 **Customizable Character Sets**
- Lowercase letters (always included)
- Uppercase letters
- Numbers
- Special symbols

📏 **Flexible Length** - Generate passwords from 4 to 30 characters

💪 **Strength Indicator** - Real-time password strength assessment with color-coded feedback:
- Weak (Red)
- Fair (Orange)
- Good (Yellow)
- Strong (Green)
- Very Strong (Green)

📋 **One-Click Copy** - Copy generated passwords to clipboard instantly

🎨 **Responsive Design** - Works seamlessly on desktop and mobile devices

## Project Structure

```
Password-GeneratorFlask/
├── password_ger.py              # Main Flask application
├── templates/
│   ├── index.html               # Home page template
│   └── gernerate.html           # Generate page template
└── README.md                    # This file
```

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/samarthrana027/Password-GeneratorFlask.git
   cd Password-GeneratorFlask
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install flask
   ```

## Usage

1. **Run the application**
   ```bash
   python password_ger.py
   ```

2. **Open in browser**
   - Navigate to `http://localhost:5000`
   - Or `http://127.0.0.1:5000`

3. **Generate passwords**
   - Click "Generate Password" from the home page
   - Adjust the length slider (4-30 characters)
   - Select character types (uppercase, numbers, symbols)
   - Click "Generate Password" button
   - Copy the result with the "Copy" button

## How It Works

### Password Generation Algorithm

The application uses a intelligent password generation algorithm that:

1. **Guarantees character diversity** - If you select character types, at least one of each type is included
2. **Maintains randomness** - Fills remaining length with random characters from the selected pool
3. **Shuffles the result** - Randomizes character positions for better security

### Strength Scoring

Password strength is calculated based on:
- Length (≥8, ≥12, ≥16 characters)
- Character type variety (uppercase, numbers, symbols)
- Maximum score: 6 points

Scoring breakdown:
- 0-2 points: Weak ❌
- 3 points: Fair ⚠️
- 4 points: Good ✓
- 5 points: Strong ✓✓
- 6 points: Very Strong ✓✓✓

## Technologies Used

- **Backend**: Flask (Python web framework)
- **Frontend**: HTML5, CSS3, JavaScript
- **Styling**: Custom CSS with CSS Grid and Flexbox
- **Icons**: Inline SVG icons
- **Fonts**: Google Fonts (Syne, DM Sans, DM Mono)

## API Routes

| Route | Method | Description |
|-------|--------|-------------|
| `/` | GET | Home page with feature overview |
| `/generate` | GET | Password generator form |
| `/generate` | POST | Generate and display password |

## Customization

### Modify Password Length Range
Edit `password_ger.py` line 363:
```python
<input type="range" name="length" id="lengthSlider"
       min="4" max="30" value="{length}">
```

### Change Color Scheme
Edit the CSS variables in `password_ger.py` lines 13-18:
```python
:root {
  --bg:#0f0f0f;              # Background color
  --accent:#e8ff47;          # Primary accent color
  --green:#4dff91;           # Success/positive color
  --text:#f0f0f0;            # Text color
}
```

### Add More Special Characters
Edit `password_ger.py` line 223:
```python
syms = "!@#$%^&*()_+-=[]{}|;:,.<>?"
```

## Browser Support

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Security Notes

⚠️ **Important**: This application generates passwords locally in your browser. No passwords are stored or transmitted to servers beyond the session.

### Best Practices
- Generated passwords are never logged
- Use HTTPS when deploying to production
- Regularly update Flask to patch security vulnerabilities

## Future Enhancements

- 🔒 Password strength meter improvements
- 📊 Generation history (client-side only)
- 🎯 Preset password profiles (PIN, passphrase, etc.)
- 🌍 Multi-language support
- 📱 Progressive Web App (PWA) capabilities
- ⚙️ Advanced options (exclude ambiguous characters, etc.)

## Troubleshooting

### Port 5000 is already in use
```bash
python password_ger.py --port 5001
```

### CSS not loading properly
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Restart the Flask server

### Template files not found
- Ensure `templates/` directory exists in the same location as `password_ger.py`
- Verify template filenames match exactly

## Contributing

Contributions are welcome! Please feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the MIT License.

## Author

**Samarth Rana** - [@samarthrana027](https://github.com/samarthrana027)

## Support

If you encounter any issues or have suggestions, please [open an issue](https://github.com/samarthrana027/Password-GeneratorFlask/issues) on GitHub.

---

**Made with ❤️ by Samarth Rana**
