# Project Management App

App link: https://task-flow-pro-365.web.app

Framework: Created Using React and Tailwind CSS.

Description: Used to manage your projects, thereby monitoring and updating the status of the project.

## Components

App.js: It contains function to add and delete the project as well as add and delete tasks. It returns the main content and the sidebar.

Button.jsx: Specialized Button component is created instead the button tag.

Input.jsx: The Input component, defined using forwardRef, renders either an <input> or <textarea> element based on the textarea prop, with common styling applied. It accepts label and other props, and forwards the ref to the underlying DOM element for direct access.

Modal.jsx: The `Modal` component, using `forwardRef`, provides a modal dialog with a `ref`-forwarded method to programmatically open the dialog. It uses `createPortal` to render the modal content into a separate DOM node identified by `modal-root`, ensuring it appears above other content.

New Project: The `NewProject` component manages a form to add a new project, utilizing `Input` components for user input and a `Modal` to alert users of missing values. It uses `useRef` to handle form element references and validates inputs before invoking the `onAdd` callback, while displaying the modal for invalid input.

New Task: The `NewTask` component provides a text input and a button to add a new task. It uses the `useState` hook to manage the input value, updates the state on input changes, and clears the input after adding the task if it's not empty.

No Project Selected : The `NoProjectSelected` component displays a message and an image when no project is selected. It includes a button to initiate adding a new project, using the `Button` component and calling the `onStartAddProject` function when clicked.

Selected Project : The `SelectedProject` component displays the details of a selected project, including its title, due date, and description. It also provides a button to delete the project and renders a `Tasks` component for managing tasks related to the project.

Side Bar : The `SideBar` component renders a sidebar with a list of projects and a button to add a new project. It highlights the currently selected project and calls `onSelectProject` when a project is clicked, while using `onStartAddProject` to handle adding new projects.

Tasks : The `Tasks` component manages and displays a list of tasks for a project. It includes a `NewTask` component for adding tasks and conditionally shows a message if there are no tasks. If tasks exist, they are listed with a button to delete each task, utilizing the `onDelete` function for removal.
