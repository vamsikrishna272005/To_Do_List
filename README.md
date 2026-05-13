# Ex03 To-Do List using JavaScript
## Date:13-05-2026
## Name:Vamsi Krishna G
## Reg no:212223220120

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
### HTML:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced To-Do List</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">

        <h1>📝 To-Do List</h1>

        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Enter your task">
            <button onclick="addTask()">Add</button>
        </div>

        <ul id="taskList"></ul>

        <div class="footer">
            Manage your daily tasks efficiently
        </div>

    </div>

    <script>

        function addTask(){

            let taskInput = document.getElementById("taskInput");
            let taskValue = taskInput.value.trim();

            if(taskValue === ""){
                alert("Please enter a task");
                return;
            }

            let li = document.createElement("li");

            let span = document.createElement("span");
            span.className = "task-text";
            span.innerText = taskValue;

            let buttonDiv = document.createElement("div");
            buttonDiv.className = "buttons";

            let completeBtn = document.createElement("button");
            completeBtn.innerText = "Done";
            completeBtn.className = "complete-btn";

            completeBtn.onclick = function(){
                span.classList.toggle("completed");
            };

            let deleteBtn = document.createElement("button");
            deleteBtn.innerText = "Delete";
            deleteBtn.className = "delete-btn";

            deleteBtn.onclick = function(){
                li.remove();
            };

            buttonDiv.appendChild(completeBtn);
            buttonDiv.appendChild(deleteBtn);

            li.appendChild(span);
            li.appendChild(buttonDiv);

            document.getElementById("taskList").appendChild(li);

            taskInput.value = "";
        }

    </script>

</body>
</html>
```
### CSS:

```
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#1e3c72,#2a5298);
    padding:20px;
}

.container{
    width:100%;
    max-width:500px;
    background:white;
    border-radius:20px;
    padding:30px;
    box-shadow:0 10px 30px rgba(0,0,0,0.3);
}

.container h1{
    text-align:center;
    margin-bottom:25px;
    color:#1e3c72;
}

.input-section{
    display:flex;
    gap:10px;
    margin-bottom:20px;
}

.input-section input{
    flex:1;
    padding:14px;
    border:2px solid #ccc;
    border-radius:10px;
    font-size:16px;
    outline:none;
    transition:0.3s;
}

.input-section input:focus{
    border-color:#2a5298;
}

.input-section button{
    padding:14px 20px;
    border:none;
    background:#2a5298;
    color:white;
    border-radius:10px;
    cursor:pointer;
    font-size:16px;
    transition:0.3s;
}

.input-section button:hover{
    background:#1e3c72;
    transform:scale(1.05);
}

ul{
    list-style:none;
}

li{
    background:#f4f4f4;
    padding:15px;
    margin-bottom:12px;
    border-radius:12px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    transition:0.3s;
}

li:hover{
    transform:translateX(5px);
    background:#e8f0ff;
}

.task-text{
    flex:1;
    font-size:17px;
}

.completed{
    text-decoration:line-through;
    color:gray;
}

.buttons{
    display:flex;
    gap:10px;
}

.complete-btn{
    background:#28a745;
    color:white;
    border:none;
    padding:8px 12px;
    border-radius:8px;
    cursor:pointer;
}

.delete-btn{
    background:#dc3545;
    color:white;
    border:none;
    padding:8px 12px;
    border-radius:8px;
    cursor:pointer;
}

.complete-btn:hover{
    background:#1f8a37;
}

.delete-btn:hover{
    background:#b52a37;
}

.footer{
    margin-top:20px;
    text-align:center;
    color:#555;
    font-size:15px;
}

@media(max-width:500px){

    .input-section{
        flex-direction:column;
    }

    .input-section button{
        width:100%;
    }

    li{
        flex-direction:column;
        align-items:flex-start;
        gap:10px;
    }

    .buttons{
        width:100%;
        justify-content:flex-end;
    }
}
```
## OUTPUT

<img width="1919" height="872" alt="image" src="https://github.com/user-attachments/assets/ce12713f-70df-4257-912e-a465e61e54a4" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
