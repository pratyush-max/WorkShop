# Task App

## Overview
The Task App is a simple web application that allows users to create and manage a list of tasks. Built with HTML, CSS (optional), and JavaScript, this application provides an intuitive interface for adding tasks, which are displayed dynamically without the need for page reloads.

## Features
- **Add Tasks**: Easily enter and add tasks to the list.
- **Dynamic Updates**: View tasks immediately as they are added.
- **User-Friendly Interface**: Simple design for easy navigation and usage.

## Technologies Used
- **HTML**: For the structure of the web application.
- **CSS**: (Optional) For styling purposes (not included in the provided code).
- **JavaScript**: To handle user interactions and dynamically update the task list.

## Installation
To run the Task App locally, follow these steps:

1. **Clone the Repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd task-app
   ```

2. **Open the HTML File**:
   Open the `index.html` file in your preferred web browser.

## Usage
1. **Adding a Task**:
   - Enter a task name in the input field labeled "Enter a new task."
   - Click the "Add Task" button or press Enter.
   - The task will be added to the table below.

2. **Viewing Tasks**:
   - All tasks added will be displayed in the table under the "Task Name" column.

## Code Explanation
The following code implements the Task App:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Task App</title>
</head>
<body>

  <table>
    <thead>
      <tr>
        <th>Task Name</th>
      </tr>
    </thead>
    <tbody id="tasks">
    </tbody>
  </table>

  <form>
    <input type="text" name="task" id="task-input" placeholder="Enter a new task">
    <button type="submit">Add Task</button>
  </form>

  <script>
    document.querySelector('form').addEventListener('submit', function(e) {
      e.preventDefault();
      var task = document.querySelector('#task-input').value;
      if (task) {
        var tasks = document.querySelector('#tasks');
        var newTask = document.createElement('tr');
        newTask.innerHTML = '<td>' + task + '</td>';
        tasks.appendChild(newTask);
        document.querySelector('#task-input').value = ''; // Clear input field
      }
    });
  </script>

</body>
</html>
```

### Code Breakdown
- **HTML Structure**:
  - A `<table>` is used to display tasks, with a header and a body for task entries.
  - A form includes an input field and a button to submit tasks.

- **JavaScript Functionality**:
  - An event listener on the form captures the submission event, preventing the default behavior.
  - The task input is retrieved, a new table row is created, and the task is appended to the task list.
  - The input field is cleared after submission for convenience.

## Contribution
Contributions are welcome! Feel free to suggest improvements, new features, or optimizations.

## License
This project is open-source and available for modification and redistribution. 

## Acknowledgements
This project serves as a basic introduction to web development, particularly focusing on handling forms and dynamic content with JavaScript. Enjoy building and expanding upon this task management application!
