let s = "A man, a plan, a canal: Panama";
let clean = s.toLowerCase().replace(/[^a-z0-9]/g, "");
console.log(clean === clean.split('').reverse().join(''));


npx create-react-app myapp
cd myapp
npm install react-router-dom
npm start

<input id="task">
<button onclick="add()">Add</button>

<ul id="list"></ul>

<script>
function add() {
    let li = document.createElement("li");

    li.innerHTML = task.value + 
    " <button onclick='del(this)'>Delete</button>";

    list.appendChild(li);
    task.value = "";
}

function del(btn) {
    btn.parentElement.remove();
}
</script>

import {BrowserRouter, Routes, Route, Link} from "react-router-dom";
function Home(){ return <h1>Home</h1>; }
function About(){ return <h1>About</h1>; }
function Contact(){ return <h1>Contact</h1>; }
export default function App(){
return(
<BrowserRouter>
<Link to="/">Home</Link>
<Link to="/about">About</Link>
<Link to="/contact">Contact</Link>
<Routes>
<Route path="/" element={<Home/>}/>
<Route path="/about" element={<About/>}/>
<Route path="/contact" element={<Contact/>}/>
</Routes>
</BrowserRouter>
);
}

import {useState} from "react";

export default function App() {
  const [product] = useState("Laptop");

  return (
    <div>
      <h1>{product}</h1>
      <button onClick={() => alert(product)}>Buy</button>
    </div>
  );
}

let s = ["h","e","l","l","o"];
console.log(s.reverse());

const express = require("express");
const app = express();

app.use(express.json());

let users = []; // temporary data

// ✅ GET (Read all)
app.get("/users", (req, res) => {
    res.send(users);
});

// ✅ POST (Create)
app.post("/users", (req, res) => {
    users.push(req.body);
    res.send("User Added");
});

// ✅ PUT (Update)
app.put("/users/:id", (req, res) => {
    users[req.params.id] = req.body;
    res.send("User Updated");
});

// ✅ DELETE (Delete)
app.delete("/users/:id", (req, res) => {
    users.splice(req.params.id, 1);
    res.send("User Deleted");
});

app.listen(3000, () => console.log("Server running"));


let n = 15;
for(let i=1;i<=n;i++){
    if(i%15===0) console.log("FizzBuzz");
    else if(i%3===0) console.log("Fizz");
    else if(i%5===0) console.log("Buzz");
    else console.log(i);
}


let nums = [3,2,2,3];
let val = 3;
nums = nums.filter(num => num !== val);
console.log(nums.length);
console.log(nums);

let s = "leetcode";
for(let i=0;i<s.length;i++){
    if(s.indexOf(s[i]) === s.lastIndexOf(s[i])){
        console.log(i);
        break;
        }}

deployment commands
git init
git add .
git commit -m "first commit"
