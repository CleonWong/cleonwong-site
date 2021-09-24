---
layout: post
title: "Custom theme in Material UI"
date: 2021-09-19 00:00:00 +0800
tags: frontend-dev
categories: drafts
pretext:
thanks:
---

Questions:

- Should I use `<Paper>` or `<div>`?

Custom theme:

- Custom theme
  - Custom typography
  - Custom colours
  - Custom buttons
- Dark and light mode

Things to cover in future:

- Custom icons

---

# TL;DR

- MUI uses the `Theme` object to specify the theme (i.e. stylistic characteristics of your React app).
- Edit the default `Theme` object using `Theme Provider` component to update it into a custom theme.

---

In this piece, I walk through how to implement a custom theme for a React (with TypeScript) app that uses Material UI (MUI) v5.0.0.

Note:

- This is a beginner-friendly article. I've included links to parts of the documentation (where necessary) that show where I got the information. _Knowing how to read documentation is very important._

# Quick setup

Let us quickly set up a project with React, TypeScript and MUI using [create-react-app](https://create-react-app.dev/). I will be using the [yarn package manager](https://yarnpkg.com/).

Open the command prompt, navigate to your desired parent folder and type in the following commands. Your React app will be created directly within this folder.

Set up the React app with TypeScript:

```zsh
$ yarn create react-app . --template typescript
```

Add MUI library:

```zsh
$ yarn add @mui/material @emotion/react @emotion/styled @mui/icons-material @mui/styles
```

After those, you should have the following folders in your parent directory:

```zsh
.
├── README.md
├── node_modules
├── package.json
├── public
├── src
├── tsconfig.json
└── yarn.lock
```

Finally, do the following to launch your newly created React app in your browser:

```zsh
$ yarn start
```

Enter `http://localhost:3000/` in your browser to view your React app.

# Understanding the default `Theme` object

The theme in MUI is used to specify all stylistic characteristics of your React app, from colour palettes, typographic stylings to button and icon sizes. MUI comes with a [default theme](https://mui.com/customization/default-theme/). It is the set of styles that you see in all MUI components by default.

## Accessing the `theme` object

The MUI global `theme` object is accessible using the [`useTheme()` hook](https://mui.com/styles/api/#usetheme-theme). The `useTheme()` hook returns the default MUI `theme` object if you do not already have a custom `theme` object created.

In `App.tsx`, import the following:

```tsx
import { createTheme } from "@mui/material/styles";
```

Within the `App()` function, add the following:

```tsx
const theme = createTheme({});
console.log(theme);
```

You should now see the entire default MUI `theme` object printed in your browser's Dev Tool console.

# Overwriting the default `theme` object

You can create a custom theme by overwriting selected parts of the default `theme` object using the [`createTheme` method](https://mui.com/customization/theming/#createtheme-options-args-theme) and passing it through the [`<ThemeProvider />` component](https://mui.com/customization/theming/#theme-provider).

One good practice is to define a `theme.tsx` file into the `/src` folder (as opposed to creating the global theme in `App.tsx`). This will keep your `App.tsx` code lighter and make your application structure cleaner.

---

- Start a new React app, console log the default theme to see that it is just a javascript object.
- Then show some components with default stylings.
- What you need to do is to change this theme object.
- How do you do that? Use the Theme Provider.
- wtf is theme provider?

- Setup
  - Typescript + MUI v5.0.0 + yarn
- Understanding themeing in MUI using MUI's default theme.
  - Show examples on how to style MUI's components using the default theme.
    - `<Paper>` (the most basic, this is just a `<div>`)
    - `<Button>`
    - `<Card>`
- Now that we understood how themeing works, explain how to edit the default theme into a custom theme.
  - Overwriting default props of existing components.
    - Where to find the available props that can be edited?
      - Look at the Component API section of the documentation, find Props and CSS sections.
  - Removing existing variants of existing compoonents.
  - Adding new variants of ecisting components.
- Show examples on how to style components using the custom theme.
