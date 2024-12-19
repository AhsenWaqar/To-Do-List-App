body {
    font-family: Arial, sans-serif;
    background-image: url('cat2.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    margin: 0;
    padding: 20px;
}

header {
    text-align: center;
}

.input-section {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
}

input[type="text"] {
    padding: 10px;
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    padding: 10px 15px;
    margin-left: 10px;
    border: none;
    border-radius: 4px;
    background-color: #28a745;
    color: white;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

.task-list {
    margin-bottom: 20px;
}

.task-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background: white;
    border: 1px solid #ccc;
    border-radius: 4px;
    margin-bottom: 10px;
}

.task-list li.completed {
    text-decoration: line-through;
    color: #888;
}

.task-counter {
    text-align: center;
}
