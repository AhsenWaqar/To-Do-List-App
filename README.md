<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>My To-Do List</h1>
    </header>
    <main>
        <section class="input-section">
            <input type="text" id="taskInput" placeholder="Add a new task...">
            <button id="addButton">Add</button>
        </section>
        <section class="task-list">
            <ul id="taskList"></ul>
        </section>
        <section class="task-counter">
            <p id="taskCount">Total Tasks: 0 | Remaining Tasks: 0</p>
        </section>
    </main>
    <script src="script.js"></script>
</body>
</html>
