# AI ROI Calculator

React application for estimating the return on investment (ROI) of adopting AI solutions. The project is bootstrapped with [Create React App](https://create-react-app.dev/) and is designed to let teams plug in their own assumptions—such as projected automation savings, model training costs, and ongoing maintenance—in order to compare different AI implementation scenarios.

The UI is still the default CRA starter while the core calculator is being designed, but the repository already has the tooling in place for rapid iteration.

## Prerequisites

- Node.js 18+ (16+ works, but the tooling is tested with 18 LTS)
- npm 8+ (ships with the Node installers mentioned above)

Check your local versions:

```bash
node --version
npm --version
```

## Getting Started

Install dependencies:

```bash
npm install
```

Run the development server on [http://localhost:3000](http://localhost:3000):

```bash
npm start
```

The development server hot-reloads as you edit files in `src/`. Lint errors show up in the terminal and browser overlay.

## Available Scripts

- `npm start` – run the dev server with hot reloading.
- `npm test` – launch Jest in watch mode (uses React Testing Library).
- `npm run build` – output a production bundle to the `build/` directory.
- `npm run eject` – copy CRA configuration files into the repo (irreversible; avoid unless you need full control).

## Project Structure

```
ai-roi-calculator/
├── public/          # Static assets served as-is (HTML shell, icons, manifest)
├── src/             # React source code (App, styles, tests)
├── package.json     # Scripts, dependencies, project metadata
└── README.md        # You are here
```

Key entry points:

- `src/App.js` – main React component; replace the placeholder UI with the calculator workflow.
- `src/App.css` and `src/index.css` – global styling hooks.
- `src/App.test.js` – starter test, expand with ROI-specific assertions.

## Implementing the Calculator

Suggested next steps once you are ready to wire up the real calculator:

1. Define the input model (e.g., implementation cost, projected savings, time-to-value) in local component state or a dedicated state manager.
2. Add helper utilities in `src/` (for example `src/lib/roi.js`) to keep math logic isolated and testable.
3. Expand the UI with form components and visualizations to help compare scenarios.
4. Mirror the calculation logic in unit tests so that refactors do not break the math.

Feel free to tailor these steps to your team's workflow; they serve as a lightweight roadmap.

## Deployment

The output of `npm run build` is a static site that can be hosted on services such as Vercel, Netlify, AWS Amplify, or any static file server. CRA includes sensible defaults for caching and asset hashing; add CI/CD to automate deployment when you are ready.

## Contributing

1. Create a feature branch from `main`.
2. Commit work with descriptive messages (follow the conventional commits spec if you already use it).
3. Ensure `npm test` passes before opening a pull request.
4. Document any new environment variables or assumptions in this README.

Issues and feature requests can be tracked in GitHub; open a discussion before large architectural changes so the team can weigh in.
