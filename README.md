document.addEventListener('DOMContentLoaded', () => {
    const taskInput = document.getElementById('taskInput');
    const addButton = document.getElementById('addButton');
    const taskList = document.getElementById('taskList');
    const taskCount = document.getElementById('taskCount');

    let tasks = [];

    const updateTaskCount = () => {
        const totalTasks = tasks.length;
        const remainingTasks = tasks.filter(task => !task.completed).length;
        taskCount.textContent = `Total Tasks: ${totalTasks} | Remaining Tasks: ${remainingTasks}`;
    };

    const renderTasks = () => {
        taskList.innerHTML = '';
        tasks.forEach((task, index) => {
            const li = document.createElement('li');
            li.textContent = task.text;
            if (task.completed) {
                li.classList.add('completed');
            }

            const checkbox = document.createElement('input');
            checkbox.type = 'checkbox';
            checkbox.checked = task.completed;
            checkbox.addEventListener('change', () => {
                task.completed = checkbox.checked;
                renderTasks();
                updateTaskCount();
            });

            const deleteButton = document.createElement('button');
            deleteButton.textContent = 'Delete';
            deleteButton.addEventListener('click', () => {
                tasks.splice(index, 1);
                renderTasks();
                updateTaskCount();
            });

            li.appendChild(checkbox);
            li.appendChild(deleteButton);
            taskList.appendChild(li);
        });
        updateTaskCount();
    };

    addButton.addEventListener('click', () => {
        const taskText = taskInput.value.trim();
        if (taskText) {
            tasks.push({ text: taskText, completed: false });
            taskInput.value = '';
            renderTasks();
        } else {
            alert('Please enter a task.');
        }
    });
});
