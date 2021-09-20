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

In this piece, I break down how to implement a custom theme for a webapp that uses Material UI (MUI) with React. Note that this tutorial is based on MUI v5.0.0.

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
