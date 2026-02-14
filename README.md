# Contact Form - My Sonic Lab

Premium contact form for audio brand websites. Built with HTML5, CSS3, vanilla JavaScript, and Node.js/Express backend.

## Features

✅ Responsive design (desktop/mobile)  
✅ Form validation (client & server)  
✅ Email integration (Nodemailer)  
✅ Accessibility (WCAG compliant)  
✅ Minimalist premium styling  
✅ Error handling & success messages  

## Project Structure

```
contact-form-mysoniclab/
├── index.html           # Main form markup
├── contact.css          # Styling
├── contact.js           # Client-side validation
├── server.js            # Express backend
├── package.json         # Dependencies
├── .env.example         # Environment template
└── README.md            # This file
```

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/shantdvs/contact-form-mysoniclab.git
cd contact-form-mysoniclab
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup environment variables
```bash
cp .env.example .env
```

Edit `.env` with your credentials:
```
EMAIL_USER=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
ADMIN_EMAIL=admin@mysoniclab.com
PORT=3000
```

### 4. Run the server
```bash
npm start
```

Visit: `http://localhost:3000`

## Configuration

### Email Setup (Gmail)

1. Enable 2-factor authentication in Gmail
2. Generate app password: https://myaccount.google.com/apppasswords
3. Add to `.env`:
   ```
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASSWORD=your-16-char-app-password
   ```

### Email Providers

Supports: Gmail, Outlook, SendGrid, AWS SES, etc.

Change in `server.js`:
```javascript
const transporter = nodemailer.createTransport({
    service: 'gmail', // or other service
    auth: { ... }
});
```

## Form Fields

- Full Name (required)
- Email (required, validated)
- Phone (optional)
- Subject (required)
- Message (required, textarea)
- Inquiry Type (dropdown)
- Country (optional)
- Privacy Policy Checkbox (required)

## Customization

### Colors
Edit `:root` in `contact.css`:
```css
:root {
    --primary-color: #000;
    --accent-color: #d4af37;
    --error-color: #e74c3c;
}
```

### Contact Information
Edit sidebar in `index.html`:
```html
<div class="info-item">
    <strong>Address</strong>
    <p>Your Address Here</p>
</div>
```

### Form Fields
Add/remove fields in `index.html` and update validation in `contact.js`

## Browser Support

- Chrome/Edge 88+
- Firefox 85+
- Safari 14+
- Mobile browsers (iOS/Android)

## Development

With nodemon:
```bash
npm run dev
```

## License

MIT

## Author

shantdvs