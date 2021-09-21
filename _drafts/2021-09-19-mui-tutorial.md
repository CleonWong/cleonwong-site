---
layout: post
title: "Teaching myself Material UI"
date: 2021-09-19 00:00:00 +0800
tags: frontend-dev
categories: tech
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

In this piece, I break down how to implement a custom theme for a webapp that uses Material UI (MUI) with React. Note that this is a tutorial for MUI v5.0.0.

The theme in MUI is used to specify all stylistic characteristics of your React app, from colour palettes, typographic stylings to button and icon sizes. MUI comes with a [default theme](https://mui.com/customization/default-theme/). It is the styles that you see in all MUI components by default.

- Start a new React app, console log the default theme to see that it is just a javascript object.
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
