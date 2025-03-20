# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

-----------------------------------------------------------------------------------------------------------------

# UI Component Library

## Project Overview
This is a **React-based UI Component Library** built using **TypeScript, Styled-Components, and Storybook**. It includes a collection of reusable UI components with **testing, linting, and Docker support** for easy deployment.

---

## Installation
### Prerequisites
Before you begin, ensure you have the following installed:
- **Node.js v18+**
- **npm v8+** or **yarn**
- **Docker (for containerization)**

### Install Dependencies

npm install
```

### Add Husky for Pre-commit Hooks

```sh
npm install husky --save-dev
npx husky install
npx husky add .husky/pre-commit "prettier --write . && eslint . --fix && npm test"
```

### Configure ESLint & Prettier

```sh
npx eslint --init

```

### Edit package.json to include:

```json
"scripts": {
  "lint": "eslint src/",
  "format:check": "prettier --check ."
},
"husky": {
  "hooks": {
    "pre-commit": "prettier --write . && eslint . --fix && npm test"
  }
}

```

### Run ESLint

npm run lint


---

## Testing with Jest & React Testing Library

This project includes unit and component testing with **Jest** and **React Testing Library**.

### Install Testing Dependencies

npm install --save-dev jest @testing-library/react @testing-library/jest-dom


### Run Tests

npm test


### Run Tests in Watch Mode

npm test -- --watch


---

## Storybook
Storybook is used to develop and showcase components in isolation.

### Install Storybook

npx storybook init


### Run Storybook Locally

npm run storybook


### Build Storybook

npm run build-storybook


---

## Husky - Git Hooks
Husky helps enforce code quality by running pre-commit checks.

### Install Husky

npx husky-init && npm install


### Enable Pre-Commit Hook

npx husky add .husky/pre-commit "npm run lint && npm test"


### Verify Husky Hooks

cat .husky/pre-commit


---

## Docker Deployment
This project includes a **Dockerfile** for containerization and deployment.

### Build Docker Image

docker build -t dogra_rakshita_coding_assignment13 .


### Run Docker Container

docker run -d -p 8018:8018 --name dogra_rakshita_coding_assignment13 dogra_rakshita_coding_assignment13


### Check Running Containers

docker ps


### Stop & Remove Container

docker stop dogra_rakshita_coding_assignment13
docker rm dogra_rakshita_coding_assignment13


---

## Troubleshooting
**Docker Error: Container Name Already Exists**

docker rm -f dogra_rakshita_coding_assignment13


**Storybook Build Issues**
- Ensure dependencies are installed correctly:

  rm -rf node_modules package-lock.json
  npm install

- Try rebuilding:

  npm run build-storybook


---

## Author
**Rakshita Dogra**  
Full Stack Developer  

