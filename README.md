# React Components & Props Lab

A small React blog site built with Vite to practice composing components, writing JSX, and passing data through props.

## Table of Contents

- [About](#about)
- [Features](#features)
- [Technologies](#technologies)
- [Getting Started](#getting-started)
- [Available Scripts](#available-scripts)
- [Project Structure](#project-structure)
- [Component Overview](#component-overview)
- [Data Flow](#data-flow)
- [License](#license)

## About

This project is a static blog landing page that demonstrates how to structure a React application using reusable components. Blog content is defined in `src/data/blog.js`, and the top-level `App` component passes that content into child components via props.

## Features

- Header section with the blog title
- About section with a logo image and blog description
- Article list rendered from an array of post objects
- Component-based architecture using React props
- Vite-powered development and build setup

## Technologies

- React
- Vite
- JSX
- CSS
- Vitest + Testing Library

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/react-components-props-vite-lab.git
   cd react-components-props-vite-lab
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

4. Open the app in your browser at `http://localhost:5173`.

## Available Scripts

- `npm run dev` - start the Vite development server
- `npm run build` - build the production bundle
- `npm run preview` - preview the production build locally
- `npm run lint` - run ESLint across the project
- `npm run test` - run the Vitest test suite

## Project Structure

```
react-components-props-vite-lab/
├── public/
├── src/
│   ├── components/
│   │   ├── About.jsx
│   │   ├── Article.jsx
│   │   ├── ArticleList.jsx
│   │   └── Header.jsx
│   ├── data/
│   │   └── blog.js
│   ├── __tests__/
│   ├── App.css
│   ├── App.jsx
│   └── main.jsx
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

## Component Overview

- `App.jsx` — root component that imports blog data and passes props to child components.
- `Header.jsx` — renders the blog title.
- `About.jsx` — displays the blog logo image and description.
- `ArticleList.jsx` — maps over the post list and renders an `Article` component for each entry.
- `Article.jsx` — shows a single article preview including title, date, and summary.

## Data Flow

Blog content is stored in `src/data/blog.js` as a JavaScript object:

- `name` — blog title
- `image` — logo image path
- `about` — blog description text
- `posts` — array of article objects

The `App` component imports this data and passes it down as props:

- `Header` receives `name`
- `About` receives `image` and `about`
- `ArticleList` receives `posts`

Each `Article` component receives `title`, `date`, and `preview` props from `ArticleList`.

## License

This project is released under the MIT License.
