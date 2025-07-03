# Developer Guide: Website Setup

This document provides details on the setup and local development of the Astro-based website for the Newcomer Handbook. The main content for the site is sourced from `README.md`.

---

## Website Setup (Astro & GitHub Pages)

This handbook is now rendered as a static website using [Astro](https://astro.build/) and automatically deployed to GitHub Pages.

**View the live site:** [https://XiyouMobile.github.io/Newcomer-Handbook/](https://XiyouMobile.github.io/Newcomer-Handbook/)

The main page of the site displays the content of this README file.

### Project Structure (Astro Specifics)

Key files and directories for the Astro setup include:

```text
/
├── .github/workflows/deploy.yml  # GitHub Actions workflow for deployment
├── public/                       # Static assets (favicons, images, etc.)
├── src/
│   └── pages/
│       └── index.mdx             # Astro page that renders this README
├── astro.config.mjs              # Astro configuration file
├── package.json                  # Project dependencies and scripts
└── README.md                     # This file (also the main content source)
```

### Local Development Commands

To run the website locally for development or preview:

1.  **Install dependencies** (if you haven't already or if `package.json` changed):
    ```sh
    pnpm install
    ```
2.  **Start the local development server**:
    ```sh
    pnpm dev
    ```
    This will usually start the site at `http://localhost:4321/Newcomer-Handbook/`. The base path `/Newcomer-Handbook/` is important for local preview to match the deployment.
3.  **Build the site for production**:
    ```sh
    pnpm build
    ```
    This will generate the static files in the `./dist/` directory.
4.  **Preview the production build locally**:
    ```sh
    pnpm preview
    ```

### How it Works

*   **Astro**: A web framework for building fast, content-focused websites.
*   **MDX**: Allows writing JSX in Markdown files, enabling component usage within Markdown. `src/pages/index.mdx` imports this `README.md` file's raw content and renders it.
*   **GitHub Actions**: Automates the build and deployment process. On every push to the `main` branch, the workflow in `.github/workflows/deploy.yml` checks out the code, installs dependencies, builds the Astro site, and deploys the output to the `gh-pages` branch, which serves the GitHub Pages site.
