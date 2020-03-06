# cra-template-library

This is based on the official base template for [Create React App](https://github.com/facebook/create-react-app).

## How-to

### 1. Create the project

  ```javascript
    npx create-react-app my-lib-name --template library
  ```

### 2. Develop the library with [Storybook](https://storybook.js.org/) (optional)
  ```javascript
    npm run storybook
  ```

  #### 2.1 Generate static documentation (optional)

  ```javascript
    npm build-storybook
  ```

### 3. Test
  ```javascript
    npm run test
  ```

### 4. Change `package.json`

  ```
  {
    ...

    "main": "dist/index.js",
    "module": "dist/index.js",
    "files": [
      "dist",
      "README.md"
    ],
    "repository": {
      "type": "git",
      "url": "git+https://[repository-location/my-lib-name].git"
    },
      "eslintConfig": {
      "extends": "react-app"
    },
    ...
    
    "description": "default description",
    "bugs": {
      "url": "https://[repository-location/my-lib-name]/issues"
    },
    "homepage": "https://[repository-location/my-lib-name]#readme",
    "keywords": [],
    "author": "[my-name]"
    }
  ```

### 5. Compile the library
  ```javascript
    npm run build
  ```

  The resulted compiled vanilla javascript is generated inside the `dist` folder

## Pre-defined folders

  - `lib`: all react components to be compiled.
  - `__tests__`: jest tests in `*.test.js` format
  - `stories`: storybook stories in `.stories.js` format

## Pre-defined packages
  - [Babel](https://babeljs.io/docs/en/babel-cli#compile-files): to compile the react project into vanilla javascript inside the `lib` folder. This will be the exported project after `npm run prepublishOnly`.
  - [Storybook](https://github.com/storybookjs/storybook): development environment for UI components
    - [Actions](https://github.com/storybookjs/storybook/tree/next/addons/actions): display data received by event handlers in Storybook
    - [Docs](https://github.com/storybookjs/storybook/tree/next/addons/docs): transform your Storybook stories into world-class component documentation
    - [Knobs](https://github.com/storybookjs/storybook/tree/next/addons/knobs): edit props dynamically using the Storybook UI
    - [Links](https://github.com/storybookjs/storybook/tree/next/addons/links): create links that navigate between stories in Storybook
    - [ViewPort](https://github.com/storybookjs/storybook/tree/next/addons/viewport): stories to be displayed in different sizes and layouts in Storybook
  - [React Testing library](https://github.com/testing-library/react-testing-library): to write maintainable tests for your React components
  - [AirBnB linting rules]()

