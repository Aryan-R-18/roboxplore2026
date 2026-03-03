# Frontend - User Registration

This folder contains the user-facing registration form for RoboXplore.

## Files

- `index.html` - Main registration page with form

## Features

- Responsive design with futuristic theme
- Animated bubble menu navigation
- Live countdown timer
- Dynamic form (4 or 5 member teams)
- File upload for payment screenshot
- Real-time validation
- Hero section with canvas animation

## How to Use

### Development

1. **Option A: Direct Open**
   - Simply open `index.html` in your browser

2. **Option B: Local Server (Recommended)**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server -p 8000
   
   # Using VS Code Live Server
   Right-click index.html → Open with Live Server
   ```

3. **Access**: Open `http://localhost:8000`

### Configuration

The API endpoint is configured in the JavaScript section of `index.html`:

```javascript
const API_URL = 'http://localhost:5000/api/registrations';
```

For production, update this to your deployed backend URL:

```javascript
const API_URL = 'https://your-backend-domain.com/api/registrations';
```

## Sections

1. **Hero** - Main landing with countdown
2. **About** - Competition mission and features
3. **Format** - Competition rules and structure
4. **Prizes** - Prize pool information
5. **Timeline** - Event schedule
6. **Registration** - Team registration form

## Form Fields

- Team Name
- Team Leader Name
- Branch
- Team Leader Registration Number
- Team Size (4 or 5 members)
- Member Names (2, 3, 4, and optionally 5)
- Payment Screenshot Upload

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Dependencies (CDN)

- Tailwind CSS
- GSAP (animations)
- Font Awesome (icons)
- Google Fonts (Oxanium, Rajdhani)

## Customization

### Colors

Edit the Tailwind config in `<script>` tag:

```javascript
colors: {
    'neon-red': '#E10600',
    'neon-blue': '#00A3FF',
    'deep-black': '#0B0B0B',
    'panel-gray': '#121212',
}
```

### Content

All text content is directly in the HTML and can be edited easily.

## Deployment

### Netlify / Vercel

1. Push to GitHub
2. Connect repository
3. Deploy (no build needed)
4. Update API_URL to production backend

### GitHub Pages

1. Push to GitHub
2. Settings → Pages → Deploy from branch
3. Update API_URL in index.html

## Notes

- Ensure backend is running before testing
- File uploads limited to 5MB
- Only JPG/PNG images accepted
- Form validates on client and server side
