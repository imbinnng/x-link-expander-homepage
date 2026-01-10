# X-Link Expander Homepage

> 🚀 Modern homepage for X.com t.co Link Expander Chrome Extension

A beautifully designed homepage showcasing the X-Link Expander Chrome extension that automatically expands t.co links on X.com (Twitter) pages, revealing their actual destinations.

## ✨ Features

- **Modern Design**: Clean, minimalist interface inspired by Vercel's design system
- **Interactive Demo**: Hover over t.co links to see real-time expansion
- **Responsive Layout**: Perfect experience on all devices
- **Smooth Animations**: Delightful micro-interactions and transitions
- **Developer Documentation**: Clear installation and usage instructions

## 🛠️ Tech Stack

- **Framework**: Svelte 5 with TypeScript
- **Build Tool**: Vite
- **Styling**: Custom CSS with Tailwind-inspired utilities
- **Deployment**: SvelteKit with auto-adapter

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/imbinnng/x-link-expander-homepage.git
cd x-link-expander-homepage

# Install dependencies
npm install

# Start development server
npm run dev

# Open your browser
# Navigate to http://localhost:5173
```

### Build for Production

```bash
# Build the application
npm run build

# Preview the production build
npm run preview
```

## 📁 Project Structure

```
src/
├── lib/
│   └── components/
│       ├── Hero.svelte          # Hero section
│       ├── Demo.svelte          # Interactive demo
│       ├── Features.svelte      # Feature showcase
│       ├── Installation.svelte  # Installation guide
│       ├── Navbar.svelte        # Navigation
│       └── Footer.svelte        # Footer
├── routes/
│   ├── +layout.svelte          # Root layout
│   └── +page.svelte           # Homepage
├── app.html                    # HTML template
└── app.css                     # Global styles
```

## 🎨 Design System

### Colors
- **Primary**: Black background with white text
- **Accent**: Grayscale palette for subtle depth
- **Links**: Blue with hover states

### Typography
- **Font**: Inter (system font stack fallback)
- **Headings**: Large, bold with gradient effects
- **Body**: Clean, readable with proper spacing

### Components
- **Cards**: Rounded corners with subtle borders
- **Buttons**: Consistent hover and focus states
- **Animations**: Smooth fly-in and fade effects

## 📱 Responsive Design

- **Mobile**: Single column layout, optimized spacing
- **Tablet**: Two-column grids where appropriate
- **Desktop**: Full multi-column layouts

## 🌐 Live Demo

Visit the live site at: https://imbinnng.github.io/x-link-expander-homepage/

## 🔧 Available Scripts

```bash
# Development
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run check        # Run TypeScript and Svelte checks

# Maintenance
npm run check:watch  # Run checks in watch mode
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by [Vercel's design system](https://vercel.com/design)
- Built with [Svelte](https://svelte.dev/)
- Icons and design patterns from modern web standards

## 🔗 Related Projects

- [X-Link Expander Chrome Extension](https://github.com/imbinnng/x-link-expander) - The main browser extension
- [Chrome Extension Documentation](https://developer.chrome.com/docs/extensions/) - Official Chrome extension development guide

---

Made with ❤️ for the X.com community