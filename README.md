# old-portfolio

[![Build Status](https://github.com/winth03/old-portfolio/actions/workflows/azure-static-web-apps-zealous-beach-0547ba900.yml/badge.svg)](https://github.com/winth03/old-portfolio/actions/workflows/azure-static-web-apps-zealous-beach-0547ba900.yml)

A personal portfolio website built with Nuxt 3, showcasing skills, projects, and blog posts. This repository serves as an archived version of a developer's past work and learning journey, including an early web project demonstrating fundamental HTML/CSS skills.

## Features

*   **Personal Introduction**: Detailed "About Me" section (`pages/index.vue`) with an age calculator and an overview of programming, game development, and web development skills.
*   **Dynamic Blog**: Supports markdown-based blog posts (`content/blog/*.md`) with dynamic routing (`pages/blog/[...slug].vue`) powered by Nuxt Content.
*   **Reusable Components**: A collection of Vue components for navigation (`components/NavMenu.vue`, `NavItem.vue`), UI elements (`components/GitHubCard.vue`, `components/content/Collapse.vue`), and more.
*   **Modern UI**: Implemented with Element Plus (`element-plus`) for rich UI components and styled using Tailwind CSS (`assets/css/tailwind.css`) for a responsive and modern aesthetic.
*   **Page Transitions**: Smooth navigation between pages with custom CSS transitions (`assets/css/main.css`) managed by global Nuxt middleware (`middleware/transitions.global.js`).
*   **CI/CD Pipeline**: Automated build and deployment to Azure Static Web Apps via GitHub Actions (`.github/workflows/azure-static-web-apps-zealous-beach_0547ba900.yml`).
*   **Historical Project**: Includes an embedded legacy project titled "Learning with Weeaboos" (`public/learningwithweaboos/index.html`), showcasing early web development skills with HTML, CSS, and basic JavaScript.
*   **Image Handling**: Utilizes an `assets/images/index.js` for structured import and export of local image assets.

## Tech Stack

This project leverages a modern web development stack:

*   **Framework**: [Nuxt 3](https://nuxt.com/) (Vue.js 3)
*   **Languages**: HTML, CSS, JavaScript, TypeScript, Vue
*   **Styling**: [Tailwind CSS](https://tailwindcss.com/), [SCSS](https://sass-lang.com/)
*   **UI Library**: [Element Plus](https://element-plus.org/en-US/)
*   **Content Management**: [@nuxt/content](https://content.nuxt.com/) (Markdown)
*   **Deployment**: Azure Static Web Apps, GitHub Pages (as an alternative deployment script)
*   **CI/CD**: GitHub Actions
*   **Icon Library**: [Nuxt Icon](https://nuxt.com/modules/icon)
*   **Utilities**: [@nuxtjs/device](https://device.nuxtjs.org/)

## Prerequisites

Before you begin, ensure you have the following installed:

*   [Node.js](https://nodejs.org/) (LTS version recommended)
*   [npm](https://www.npmjs.com/) (comes with Node.js) or [Yarn](https://yarnpkg.com/) or [pnpm](https://pnpm.io/)

## Installation

To get a local copy up and running, follow these simple steps:

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/winth03/old-portfolio.git
    cd old-portfolio
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    # or yarn install
    # or pnpm install
    ```

## Usage

### Local Development

To run the project in development mode with hot-reloading:

```bash
npm run dev
# or yarn dev
# or pnpm dev
```

The application will typically be accessible at `http://localhost:3000`.

### Building for Production

To build the application for production deployment:

```bash
npm run build
# or yarn build
# or pnpm build
```

This command generates the `.output` directory with the production-ready build.

### Generating Static Site

To generate a static version of the site (for hosting on platforms like GitHub Pages, Azure Static Web Apps, etc.):

```bash
npm run generate
# or yarn generate
# or pnpm generate
```

This command populates the `.output/public` directory with the static files.

### Previewing the Production Build

To preview the built application locally:

```bash
npm run preview
# or yarn preview
# or pnpm preview
```

## Project Structure

The repository is organized into the following key directories and files:

```
.github/
└── workflows/                      # GitHub Actions CI/CD workflows
    └── azure-static-web-apps-...yml  # Azure Static Web Apps deployment configuration
assets/
├── css/                            # Global CSS files (Tailwind, main transitions)
├── images/                         # Static image assets, with index.js for module export
components/
├── content/                        # Components specifically for Nuxt Content (e.g., Prose elements)
└── ...                             # Reusable Vue components (e.g., GitHubCard.vue, NavMenu.vue)
content/
└── blog/                           # Markdown files for blog posts
layouts/
└── default.vue                     # Default layout for pages
middleware/
└── transitions.global.js           # Global Nuxt middleware for page transitions
pages/
├── blog/                           # Blog listing and dynamic blog post pages
│   ├── [...slug].vue               # Dynamic route for individual blog posts
│   └── index.vue                   # Blog list page
├── index.vue                       # Main "About Me" and skills showcase page
└── tour.vue                        # Another example page
public/
├── learningwithweaboos/            # Legacy project, a static HTML/CSS/JS site
│   ├── img/                        # Images for the legacy project
│   └── index.html                  # Homepage of the legacy project
├── pdf/                            # Static PDF documents
└── ...                             # Other static assets
server/
└── api/                            # Backend API routes (e.g., user.js)
nuxt.config.ts                      # Nuxt 3 configuration file
package.json                        # Project dependencies and scripts
tailwind.config.js                  # Tailwind CSS configuration
tsconfig.json                       # TypeScript configuration
```

## License

No explicit license is provided for this repository. Please contact the repository owner for licensing information.