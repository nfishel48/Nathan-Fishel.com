# Nathan-Fishel.com

[![Netlify Status](https://api.netlify.com/api/v1/badges/f41c29e3-13b1-47c6-b772-3b8d61721728/deploy-status)](https://app.netlify.com/sites/quizzical-wing-c55f54/deploys)

## Overview

Personal portfolio and blog website for Nathan Fishel, Cloud DevOps Engineer. This site showcases professional experience, technical expertise, and insights on cloud technologies, DevOps practices, and software engineering.

## Built With

- **[Hugo](https://gohugo.io/)** - Fast and flexible static site generator
- **[Gokarna Theme](https://github.com/526avijitgupta/gokarna)** - Clean and minimalist Hugo theme
- **[Netlify](https://www.netlify.com/)** - Continuous deployment and hosting
- **[Plausible Analytics](https://plausible.io/)** - Privacy-focused web analytics

## Features

- 📝 Technical blog posts on cloud, DevOps, and software engineering topics
- 👨‍💻 Professional portfolio and experience showcase
- 📧 Contact form for professional inquiries
- 🏷️ Tag-based content organization
- 📱 Fully responsive design
- 🚀 Fast page loads and optimized performance
- 🔒 Privacy-respecting analytics

## Local Development

### Prerequisites

- Hugo Extended version (v0.80.0 or later)
- Git

### Getting Started

1. Clone the repository:
```bash
git clone https://github.com/nfishel48/Nathan-Fishel.com.git
cd Nathan-Fishel.com
```

2. Navigate to the Hugo project directory:
```bash
cd NateFishel
```

3. Start the Hugo development server:
```bash
hugo server -D
```

4. Open your browser and navigate to `http://localhost:1313`

### Building for Production

To generate the static site:
```bash
hugo --minify
```

The generated files will be in the `public/` directory.

## Content Structure

```
NateFishel/
├── content/
│   ├── about/       # About page content
│   ├── contact/     # Contact form page
│   └── posts/       # Blog posts
├── static/
│   ├── css/         # Custom CSS styles
│   ├── images/      # Images and media
│   └── scripts/     # JavaScript files
├── themes/          # Hugo themes
└── config.toml      # Site configuration
```

## Deployment

This site is automatically deployed to Netlify when changes are pushed to the main branch. Every commit triggers a new build and deployment.

## Contributing

While this is a personal website, suggestions and feedback are welcome. Feel free to open an issue if you notice any problems or have recommendations.

## License

The content of this website is © Nathan Fishel. The underlying source code used to format and display that content is licensed under the MIT License.

## Contact

- **Website:** [nathanfishel.com](https://nathanfishel.com)
- **LinkedIn:** [Nathaniel Fishel](https://www.linkedin.com/in/nathaniel-f-722a72165/)
- **GitHub:** [@nfishel48](https://github.com/nfishel48)

## Acknowledgments

- Hugo community for the excellent static site generator
- Netlify for providing reliable hosting and CI/CD
- All open-source contributors who make projects like this possible