# Kelvin's Portfolio

A modern, professional portfolio website built with Vue 3, Vite, and Tailwind CSS. Inspired by professional developer portfolios with a sleek dark theme and smooth animations.

## Features

- **Responsive Design**: Fully responsive and mobile-friendly
- **Modern UI**: Dark theme with gradient accents and smooth transitions
- **Sections**:
  - Hero section with call-to-action buttons
  - About me with core skills
  - Work experience timeline
  - Notable projects showcase
  - Contact/footer section
  - Sticky navigation with mobile menu

## Tech Stack

- **Frontend**: Vue 3 (Composition API)
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Icons**: Inline SVGs

## Getting Started

### Prerequisites

- Node.js (v16+)
- npm or yarn

### Installation

```bash
# Install dependencies
npm install
```

### Development

```bash
# Start development server
npm run dev
```

The portfolio will be available at `http://localhost:5173`

### Build for Production

```bash
# Build the project
npm run build

# Preview production build
npm run preview
```

## Customization Guide

### 1. Update Personal Information

Edit the following components to add your information:

#### `src/components/Hero.vue`
- Change your name and headline
- Update location
- Modify call-to-action links

#### `src/components/About.vue`
- Update personal bio
- Add/remove skills as needed
- Customize the skills list array

#### `src/components/Experience.vue`
- Add your work experience
- Update `experiences` array with your jobs
- Include project descriptions and technologies

#### `src/components/Projects.vue`
- Add your projects
- Update `projects` array with your work
- Add GitHub and live demo links
- Change project icons

#### `src/components/Footer.vue`
- Update email address
- Add your social media links (LinkedIn, GitHub, etc.)
- Modify copyright year

#### `src/components/Navigation.vue`
- Change the logo/name at the top

### 2. Colors and Theme

Edit `tailwind.config.js` to customize colors:

```javascript
colors: {
  primary: '#3b82f6',  // Change primary color
  dark: '#0f172a',     // Change dark background
  'dark-secondary': '#1e293b',
}
```

### 3. Add Images/Assets

- Place images in `src/assets/`
- Update components to use `<img>` tags
- For project thumbnails, add image URLs to the `projects` array in `src/components/Projects.vue`

### 4. Update Meta Tags

Edit `index.html` to update:
- Title
- Description
- Theme color
- Favicon

## Project Structure

```
src/
├── components/
│   ├── Navigation.vue    # Top navigation bar
│   ├── Hero.vue          # Hero/landing section
│   ├── About.vue         # About section with skills
│   ├── Experience.vue    # Work experience timeline
│   ├── Projects.vue      # Projects showcase
│   └── Footer.vue        # Footer and contact section
├── App.vue               # Main app component
├── main.js              # Vue app entry point
└── style.css            # Global styles and Tailwind
```

## Deployment

This portfolio can be deployed to various platforms:

### Vercel (Recommended)
```bash
npm install -g vercel
vercel
```

### Netlify
1. Build the project: `npm run build`
2. Deploy the `dist` folder to Netlify

### GitHub Pages
Update `vite.config.js` with your repository name, then:
```bash
npm run build
```

## Performance Tips

- The design uses CSS gradients for performance
- Use WebP or compressed images when adding project thumbnails
- Lazy load images for better performance
- Consider adding smooth scroll behavior (already included)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This portfolio template is open source and available under the MIT License.

## Questions?

Feel free to customize this template to match your personal brand and preferences!
