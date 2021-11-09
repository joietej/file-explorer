# Getting Started with File Explorer Test solution

## Requirements
- [Design](https://www.figma.com/proto/4v2vqqsnubWyedOb0bZuVU/File-Selector-case?node-id=1%3A1944&viewport=1477%2C398%2C1.2320507764816284&scaling=min-zoom&page-id=0%3A1)
- [Use case](https://reoso.notion.site/File-Selector-case-7fb10e9fa9f242e9b30228dcaca7eb87)

## CI / CD
- [Project Vercel]() 
- [Portal])
## Bootstrap
This project was bootstrapped with [Vite](https://vitejs.dev/).

## Assumptions & Comments
- Sample Data
  - MimeType and file extension mismatched hence using file extension to determine file type.
  - Image urls are not accusable hence using file icons instated of image.
- UI / UX
  - Fonts & Colors are not 100% matched with given design.
  - Used overlay to create model dialog.
  - By default dialog is centered on screen.
  - Clicking outside the dialog closes the dialog.
## Libraries

This project uses libraries which are available for Vue and React for seamless transition.
- [Headeless UI](https://headlessui.dev)
- [Tailwind CSS](https://tailwindcss.com)
- [Testing Library](https://testing-library.com)

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles Vue in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://vitejs.dev/guide/static-deploy.html) for more information.


## Learn More

You can learn more in the [Vite](https://vitejs.dev/guide/).

To learn Vue, check out the [Vue documentation](https://v3.vuejs.org/guide/introduction.html).
