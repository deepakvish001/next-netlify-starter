# LaunchEdge

LaunchEdge is a compact Next.js and Netlify application baseline for teams that want a clear starting point for production-oriented web projects. It currently provides a Next.js 12 application, reusable header and footer components, global and component-scoped styling, Cypress browser tests, absolute imports, and Netlify build configuration.

> The repository is being evolved from a minimal starter into a documented, tested, and deployment-ready application foundation.

## Current capabilities

- Next.js pages-based application structure
- React 18 user interface
- Reusable layout components
- CSS Modules and global styles
- Cypress end-to-end test baseline
- Netlify build configuration
- Absolute import support through `jsconfig.json`
- Automated dependency update configuration

## Technology stack

| Area | Technology |
| --- | --- |
| Framework | Next.js 12 |
| UI | React 18 |
| Styling | CSS and CSS Modules |
| Browser testing | Cypress 10 |
| Hosting | Netlify |
| Package manager | npm |

## Project structure

```text
components/          Reusable interface components
cypress/e2e/         Browser-level tests
pages/               Next.js routes and app entry point
public/              Static assets
styles/              Global styles
netlify.toml         Netlify build settings
cypress.config.js    Cypress configuration
```

## Prerequisites

- Node.js 16 or newer for the current dependency baseline
- npm 8 or newer

## Local setup

```bash
git clone <repository-url>
cd <repository-directory>
npm install
npm run dev
```

Open `http://localhost:3000`. Changes under `pages`, `components`, and `styles` reload automatically during development.

## Available commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the local Next.js development server |
| `npm run build` | Create a production build |
| `npm run export` | Export supported routes as static files |
| `npx cypress open` | Run Cypress interactively |
| `npx cypress run` | Run Cypress in headless mode |

## Netlify deployment

The included `netlify.toml` runs `npm run build`, publishes the `.next` output, and loads the Cypress build plugin. Connect the repository to a Netlify site, review the detected build settings, and deploy from the default branch. Pull requests can then receive isolated deploy previews.

## Configuration

The baseline does not require application secrets. Future environment variables should be documented in `.env.example`, configured in the hosting dashboard, and never committed with real credentials.

## Roadmap

Planned work includes a modern framework upgrade, TypeScript migration, accessible navigation, reusable page metadata, error boundaries, loading states, structured logging, environment validation, stronger Cypress coverage, unit tests, linting, formatting, security headers, performance budgets, continuous integration, and deployment documentation.

## Contributing

Create focused branches from `main`, include tests for behavior changes, confirm `npm run build` succeeds, and describe deployment or configuration impact in the pull request. Keep unrelated refactors separate so changes remain easy to review and merge.

## License

Retain all license notices and third-party attribution files distributed with the project.