# Developer Portfolio
This is a remake of my portfolio: [ellisenobun.com](https://www.ellisenobun.com), 
which was built using only ReactJS. This remake takes a 
slightly different approach, resulting in a more SEO, 
accessible and performant outcome.

> Desktop View - Light Mode

<img width="1240" alt="Screenshot 2021-02-22 at 12 09 01" src="https://user-images.githubusercontent.com/15114201/108706638-cd53b200-7506-11eb-86c5-fb936b4f333e.png">

> Desktop View - Dark Mode

<img width="1240" alt="Screenshot 2021-02-22 at 12 10 03" src="https://user-images.githubusercontent.com/15114201/108706723-eeb49e00-7506-11eb-8a63-e805d0d6e0a8.png">

## Technology Used
- NextJS
    - Server Side Rendering
    - Static Generation
    - Image optimization feature
    - Built in typescript, css module & scss support
    

- TypeScript
    - Javascript in the "right" context
    

- Tailwind CSS
    - Intuitive CSS
    

- next-themes
    - Allows for dynamically changing theme color
    

- Framer Motion
    - Cool Animations

## Milestones 
- [x] Project Setup
    - [x] Install typescript: `npm i -D typescript @types/react @types/node`
    - [x] Install tailwindcss: ` npm install -D tailwindcss@latest postcss@latest autoprefixer@latest`
    - [x] Initialize tailwindcss & postcss config: `npx tailwindcss init -p`
    - [x] Remove unused styles in production (tailwindcss.config.js).
    - [x] Include Tailwind in global styles.
- [x] Setup responsiveness (mobile and desktop)
- [x] Sidebar Component
    - [ ] Theme mode (dark / light)
- [x] Create the Navbar
    - [x] Navbar should have the about, projects, and resume pages 
    - [x] Keep track of the active element of each page. Make sure its a `strong` string type (useState<string>(''))
    - [x] If the selected currentItem is not the activeItem, setActiveItem to current item when it's selected.
    - [x] The current activeItem should be displayed on the left-hand side of the navbar.
    - [x] Ensure that the home route did mount, to ensure the route path is equal to the default current item.
- [x] Setup data service on the root directory to hold all the data.
    - [x] Create a typescript interface in `services/types.ts` to describe the shape of the object data.
- [x] Create an api for the services: `api/services` - For good measure.
    - [x] Implement the `getServerSideProps()` to fetch the service data via the api available to the home page as props.
- [x] Display the interface in the home page.
    - [x] Create a ServiceCard component
    - [x] Create function to format HTML in the strings.
- [x] Setup Resume Page
    - [x] In `types.ts`, create the interface for the skill bars - Name, Level, Icon.
    - [x] In `data.ts`, create an array for the interface. One for the Lang & Frameworks, and other for Tools.
    - [x] Resume should have Experience, Education, Frameworks & Languages, Tools component.
    - [x] Setup interfaces and components for the resume page.
    - [x] Display information for resume page.
- [x] Implement Dark Mode
    - [x] Change `dark mode` in tailwind.config.js to `class`. This is for manual toggling.
    - [x] Install `next-themes`.
    - [x] Wrap the application in `_app` with the `ThemeProvider`.
    - [x] Add the class attribute to the provider.
    - [x] Keep track of the theme color in Sidebar using hooks.
    - [x] Create function to change theme.
- [ ] Setup filter
    - [ ] Filter should be displayed below the Navbar
    - [ ] Filter should be displayed only when on the projects page.

> Project Page
- [x] Set up the interface for projects data in `types.ts`.
- [x] Set up the data for projects in `data.ts`.
- [x] Create a project card component.
- [x] Loop through the project data in projects.tsx, and make data available to the card component.
- [x] Display projects in the card component.
    - [x] Create another section, that shows the single project.
    - [x] Implement logic to display single project when parent project is clicked.
        - [x] Keep track of the single project. The initial state is false.
        - [x] When the parent image is clicked, show the single project - set state to true.
- [x] Create project navbar elements component
    - [x] Project Navbar component, should have a function component that pulls Category data from data types.
    - [x] Keep track of Navbar links in the Projects component, so that when each is clicked, it shows the projects associated with it.
