# CODTECH-Task1
TASK-1: TO DO LIST APP using html,css and javascript


![Uploading Screenshot 2024-07-19 133816.png…]()



NAME : JENIFER Y
COMPANY : CODTECH IT SOLUTIONS
ID: CT4WD2714
DOMAIN : WEB DEVELOPMENT
DURATION : JUNE 20-JULY 20
MENTOR :MUZAMMIL

OVERVIEW OF MY PROJECT:
PURPOSE : to create an interactive web application of todo list,which enhanches certain features listed below

Features:
Adding tasks
Marking tasks as complete
Deleting tasks

Usage
Explain how users can interact with the app. Provide step-by-step instructions on how to perform common actions:
Adding a new task
Marking a task as complete
Deleting a task

CODE EXPLANATION:
Explanation:
<!DOCTYPE html>:

Declares the document type and specifies that this is an HTML5 document.
<html lang="en">:

Defines the root element of the HTML document and specifies the language as English (en).
<head>:

Contains meta-information about the document and links to external resources (meta, title, link).
<meta charset="UTF-8">:

Specifies the character encoding for the document as UTF-8, ensuring compatibility with a wide range of characters.
<meta name="viewport" content="width=device-width, initial-scale=1.0">:

Sets the viewport properties to ensure proper scaling on various devices, accommodating different screen sizes.
<title>To do list app</title>:

Sets the title of the web page displayed in the browser tab or title bar.
<link rel="stylesheet" href="style.css">:

Links an external CSS file (style.css) to style the content and layout of the HTML document.
<body>:


Applies styles to all elements (*), setting margin and padding to zero (margin: 0; padding: 0;), using the 'Poppins' font as default (font-family: 'poppins', sans-serif;), and ensuring the box-sizing property includes padding and border in the element's total width and height calculations (box-sizing: border-box;).
.container 

Defines the styling for a container element that wraps the entire content (width: 100%; min-height: 100vh;). It sets a background gradient (background: linear-gradient(335deg, #C4DFE6, #66A5AD);) and adds padding (padding: 10px;).
.todo-app 

Styles the main todo list application container (width: 100%; max-width: 540px; background-color: whitesmoke;). It centers this container on the page (margin: 100px auto 20px;), adds internal padding (padding: 40px 30px 70px;), and rounds the corners with a border-radius (border-radius: 10px;).
.row 

Styles the row within the todo app (display: flex; align-items: center; justify-content: space-between; background-color: #edeef0; padding: 3px; border-radius: 20px; margin-bottom: 25px; margin-top: 10px;). It uses Flexbox to arrange items, adds background color, padding, and rounded corners.
input 

Styles the input field (flex: 1; border: none; outline: none; background: transparent; padding: 8px; font-size: 14px;). It spans the full width (flex: 1;), removes borders and outlines, sets a transparent background, and adjusts padding and font size.
button 

Defines styles for the button (border: none; outline: none; padding: 16px 50px; background: #ff5945; color: #fff; font-size: 16px; cursor: pointer; border-radius: 40px;). It removes borders and outlines, sets padding, background color, text color, font size, cursor type, and border-radius.
ul li :

Styles list items within the unordered list (list-style: none; font-size: 17px; padding: 12px 8px 12px 50px; user-select: none; cursor: pointer; position: relative;). It removes default list styles, sets padding, prevents text selection (user-select: none;), adds a pointer cursor, and positions items relatively.
ul li::before :

Adds a pseudo-element (::before) to list items, representing an unchecked checkbox (content: ''; position: absolute; height: 28px; width: 28px; border-radius: 50%; background-image: url(images/unchecked.png); background-size: cover; background-position: center; top: 12px; left: 8px;).
ul li.hidden :

Styles list items with a class of hidden (e.g., completed tasks) (color: #555; text-decoration: line-through;). It changes text color to gray (#555) and applies a line-through text decoration.
ul li.hidden::before :

Modifies the pseudo-element (::before) of hidden list items to display a checked checkbox (background-image: url(images/checked.png);).
ul li span :

Styles a span element within list items (position: absolute; right: 0; top: 5px; width: 50px; height: 40px; font-size: 22px; color: #555; line-height: 40px; text-align: center; border-radius: 50%;). It positions the span at the top-right, sets dimensions, font size, color, text alignment, and adds rounded corners.
ul li span:hover { ... }:

Adds a hover effect to the span element within list items (background: bisque;). It changes the background color to bisque when the span is hovered over.
Summary:
Global Reset and Styling: The * selector resets margins and paddings, sets a default font, and ensures box-sizing consistency.

Layout and Containers: .container and .todo-app define overall layout and styling for the todo list application, including background colors, padding, and positioning.

Input and Button: input and button styles ensure a consistent look and feel for user input and interaction elements, such as background colors, padding, and cursor styles.

List Styling: ul li and related styles customize the appearance of list items, including checkboxes, text styles, decorations for completed tasks, and interactive elements like hover effects.

Input and List Initialization: Get references to the input box (inputBox) and list container (listContainer) elements using getElementById.

Task Addition: Define addTask function to check if the input is empty; if not, create a new list item (li), append it to listContainer, and add a close button (span) to each task.

Event Handling: Use addEventListener on listContainer to toggle task completion (hidden class) when clicking on a list item (LI) or remove a task when clicking on its close button (SPAN).

Data Persistence: Implement saveData function to store task list HTML in localStorage using setItem, ensuring tasks persist across page reloads.

Data Retrieval: Implement showTask function to retrieve task list HTML from localStorage using getItem and display it in listContainer.

Initialization: Call showTask function at the end to display previously saved tasks when the page loads, ensuring continuity of task management across sessions.

Contains the main content of the HTML document that is visible to users in the web browser.
<div class="container">:

Acts as a container element, often used for layout purposes to group content.
<div class="todo-app">:

Represents the main section of the todo list application.
<h1 style="text-align: center;"> TO DO LIST 📝</h1>:

Displays a centered heading (h1 element) with the text "TO DO LIST 📝", serving as the title of the todo list app.
<div class="row">:

Defines a row within the todo app, typically used for organizing elements horizontally.
<input type="text" id="input-box" placeholder="Enter your task">:

Provides an input field (input element) where users can type their tasks. It has an id of input-box for JavaScript reference and displays a placeholder text "Enter your task" to guide user input.
<button onclick="addTask()">ADD</button>:

Creates a button (button element) labeled "ADD". When clicked (onclick attribute), it triggers the addTask() function, which is expected to be defined in the linked JavaScript file (script.js).
<ul id="list-container">:

Defines an unordered list (ul element) with an id of list-container. This is where tasks will be dynamically added as list items (li elements).
`<!--<li class="hidden">Task 1</li>

 <li>Task 2</li>
 <li>Task 3</li>-->`:
- These lines are commented out (`<!-- -->`), meaning they are not active in the app. They represent example list items (`li` elements) that could be part of the todo list.
<script src="script.js"></script>:

Links an external JavaScript file (script.js) to the HTML document. This file contains the logic and functions to handle task management, such as adding tasks dynamically to the list.
Summary:
Structure: The HTML document follows a standard structure with <!DOCTYPE html>, <html>, <head>, <title>, <meta>, and <link> tags providing essential metadata and linking to external resources.

Content: Within the <body> tag, elements like <div>, <h1>, <input>, <button>, <ul>, and <li> are used to structure and display the todo list application interface.

Functionality: JavaScript (script.js) is linked to enable dynamic behavior, such as adding tasks when the user clicks the "ADD" button (onclick="addTask()") and managing tasks within the list (<ul>).








