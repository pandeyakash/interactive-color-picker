# Interactive Color Picker

## Description

This is a simple **React-based** interactive color picker app. It allows users to input a color in hexadecimal (HEX) format, and displays a square with the selected color dynamically. The app uses React's functional components and state management to handle user input and update the UI in real-time.

## Features

- **Dynamic Color Display**: Users can input a HEX color code, and the app displays the corresponding color in a square.
- **Responsive UI**: The color picker input and display area are styled to be user-friendly and responsive.

## Components

### 1. `ColorInput`

This component is responsible for rendering the input field where users can enter a color in HEX format.

- **Props**:
  - `fn`: This prop expects a function to handle the onChange event of the input. When the user enters a value, it triggers the event to update the state.

### 2. `DisplayColor`

This component is responsible for displaying a square whose background color corresponds to the user's input.

- **Props**:
  - `color`: The color value is passed down as a prop from the parent component, which dynamically sets the background color of the square.

### 3. `App`

The main component that ties everything together. It maintains the state of the current color (`color`), passes event handlers to the `ColorInput` component, and renders the `DisplayColor` component.

- **State**:

  - `color`: A string representing the current HEX color value (default is black, represented as `'000'`).

- **Event Handler**:
  - `clickHandle`: Handles the change event from the input field and updates the state with the new color entered by the user.

## How It Works

1. The app consists of two main elements: a color input field and a square that changes color based on the input.
2. When the user enters a valid HEX color code (e.g., `FF5733`), the color in the square changes dynamically.
3. The color input is handled using React's `useState` hook, and the entered value is passed as a prop to the `DisplayColor` component.
4. The color code is applied as an inline style to the square's background, so any valid HEX code will reflect in real-time.

## How to Use

1. Open the app in your browser.
2. Enter a color in the input field using a valid HEX color code (without the `#`).
3. The square will change to the color you have entered.

### Example HEX Codes:

- Red: `FF0000`
- Green: `00FF00`
- Blue: `0000FF`
- Black: `000000`
- White: `FFFFFF`

## Installation

This app uses React via CDN, so there's no need to install any additional dependencies. Just include the necessary scripts for **React**, **ReactDOM**, and **Babel** to transpile the JSX.

## How to Run

1. Download or copy the provided HTML code.
2. Open the HTML file in any modern web browser.
3. The app will load and render automatically.

## Technologies Used

- **React**: A JavaScript library for building user interfaces.
- **ReactDOM**: Used to render React components into the DOM.
- **Babel**: Used for compiling JSX code directly in the browser.
- **HTML/CSS**: For the basic structure and styling of the app.
