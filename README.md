# My Vue 3 Project

This is a Vue 3 project created with Vite, TypeScript, and ESLint.

## Project Structure

```
my-vue3-project
├── public
│   └── index.html          # Main HTML file for the application
├── src
│   ├── assets              # Static assets (images, fonts, stylesheets)
│   ├── components
│   │   └── HelloWorld.vue  # HelloWorld component
│   ├── views
│   │   └── Home.vue        # Home view component
│   ├── App.vue             # Root component of the application
│   └── main.ts             # Entry point of the application
├── .eslintrc.js            # ESLint configuration
├── .gitignore              # Git ignore file
├── index.html              # Duplicate of public/index.html for development
├── package.json            # Yarn configuration and dependencies
├── tsconfig.json           # TypeScript configuration
└── vite.config.ts          # Vite configuration
```

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd my-vue3-project
   ```

2. **Install dependencies:**
   ```bash
   yarn install
   ```

3. **Run the development server:**
   ```bash
   yarn dev
   ```

4. **Open your browser and navigate to:**
   ```
   http://localhost:3000
   ```

## Usage

- Modify the components in the `src/components` directory to customize your application.
- Add static assets in the `src/assets` directory.
- Update the routing and layout in `src/App.vue`.

## Linting

To run ESLint and check for code quality, use:
```bash
yarn lint
```

## Build

To build the application for production, run:
```bash
yarn build
```

This will generate the production-ready files in the `dist` directory.