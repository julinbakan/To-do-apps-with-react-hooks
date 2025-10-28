

🧩 
Make a new React app
👉 In terminal:

npx create-react-app todo-app
Go into the folder

cd todo-app
Start the app

npm start
Open App.js
Delete everything inside and start fresh.

Import React and useState

import React, { useState } from "react";
Make two states

const [task, setTask] = useState("");
const [list, setList] = useState([]);
Add new task

const addTask = () => {
  setList([...list, task]);
  setTask("");
};
Show all tasks

{list.map((item, i) => (
  <p key={i}>{item}</p>
))}
Add input box and button

<input value={task} onChange={(e) => setTask(e.target.value)} />
<button onClick={addTask}>Add</button>
See your tasks appear on screen! 🎉
