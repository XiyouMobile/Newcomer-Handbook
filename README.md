# XiyouMobile Newcomer Handbook (Astro Version)

This project uses [Astro](https://astro.build/) to build a static website, displaying content from Markdown files. The main page (`index.mdx`) currently displays the content of this README.

The site is automatically deployed to GitHub Pages upon pushes to the `main` branch.

You can view the deployed site at: [https://XiyouMobile.github.io/Newcomer-Handbook/](https://XiyouMobile.github.io/Newcomer-Handbook/)

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── .github/workflows/deploy.yml  # GitHub Actions workflow for deployment
├── public/                       # Static assets (images, favicons, etc.)
├── src/
│   └── pages/
│       └── index.mdx             # Main page, renders README.md content
├── astro.config.mjs              # Astro configuration file
├── package.json                  # Project dependencies and scripts
├── pnpm-lock.yaml                # Exact versions of dependencies
└── README.md                     # This file
```

Astro looks for `.astro`, `.md`, or `.mdx` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command            | Action                                           |
| :----------------- | :----------------------------------------------- |
| `pnpm install`     | Installs dependencies                            |
| `pnpm dev`         | Starts local dev server at `localhost:4321`      |
| `pnpm build`       | Build your production site to `./dist/`          |
| `pnpm preview`     | Preview your build locally, before deploying     |
| `pnpm astro ...`   | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro --help`| Get help using the Astro CLI                     |

## 👀 Want to learn more about Astro?

Feel free to check [Astro's documentation](https://docs.astro.build) or jump into their [Discord server](https://astro.build/chat).
