# React + TypeScript + Vite

# Harshith - Repository Analysis

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is enabled on this template. See [this documentation](https://react.dev/learn/react-compiler) for more information.

Note: This will impact Vite dev & build performances.

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

# Developer contributions

## Differences between forking and cloning 
| Sl. No. | Forking | Cloning |
| --- | --- | --- |
| 1. | Creates a copy of the original repository under the name of the person who forked the repository on cloud (Github) | Clones/downloads the contents of a repository from a remote server into the user's laptop which the user can modify offline |
| 2. | Usually used to contribute to a project/repository owned by someone else | It is used to write, test, debug and run the code offline |
| 3. | The user would finish their task and then submit a PR/MR to merge the new code into the original codebase | The user would pull or push the code directly (To a different branch usually, if on production, say feature, or a forked version of the codebase) to the repository |

## Commonly used git commands:
- `git branch`: Lists all the branches in the local repository, the one next to a '*' is the branch you are currently on
- `git add <path_to_file_from_root>`: Adds the file to the staging area, ready to be committed, use `git add .` to add all files to the staging area
- `git commit`: Used to commit the files from the staging area, use the flag `-m "<Your-message>"` to add a message to the commit
- `git checkout <branchname>`: Used to checkout the branch mentioned
- `git branch <branchname>`: Used to create a new branch 
- `git push <remote> <branch>`: Used to push the local commits to the remote repository to the specified branch (can use -u to make it upstream)
