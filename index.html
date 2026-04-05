<!DOCTYPE html>  
<html lang="de">  
<head>  
  <meta charset="UTF-8">  
  <title>Familien Punkte</title>  
  <style>  
    body { font-family: Arial; background: #f2f2f2; text-align: center; margin:0; }  
    h1 { background: #4CAF50; color: white; padding: 15px; margin: 0; }  
    .top { margin: 20px; }  
    input { padding:8px; font-size:14px; margin:3px; border-radius:6px; border:1px solid #ccc; }  
    button { padding:8px; margin:3px; border:none; border-radius:8px; cursor:pointer; }  
    .addBtn { background:#4CAF50; color:white; }  
    .green { background:#4CAF50; color:white; }  
    .red { background:#f44336; color:white; }  
    .orange { background:orange; color:white; }  
    .card { background:white; margin:15px auto; padding:15px; border-radius:12px; width:260px; box-shadow:0 4px 10px rgba(0,0,0,0.1); }  
    .name { font-size:20px; font-weight:bold; }  
    .error { color:red; font-size:12px; }  
  </style>  
</head>  
<body>  
  
<h1>📱 Familien Punkte</h1>  
  
<div class="top" id="adminControls">  
  <input type="text" id="nameInput" placeholder="Name eingeben">  
  <button class="addBtn" onclick="addUser()">Hinzufügen</button>  
</div>  
  
<div id="users"></div>  
  
<script>  
// --- Nutzer + Geräte ---  
let users = JSON.parse(localStorage.getItem("users")) || [];  
let devices = JSON.parse(localStorage.getItem("devices")) || [];  
  
// Gerät-ID für dieses Gerät  
let deviceID = localStorage.getItem("deviceID");  
if(!deviceID){  
  deviceID = 'dev-' + Date.now() + '-' + Math.floor(Math.random()*1000);  
  localStorage.setItem("deviceID", deviceID);  
  
  // Rolle zuweisen  
  let role;  
  if(devices.length === 0) role = "add"; // erstes Gerät darf Punkte hinzufügen  
  else if(devices.length === 1) role = "subtract"; // zweites Gerät darf Minuten abziehen  
  else role = "view"; // alle anderen nur sehen  
  
  devices.push({id: deviceID, role: role});  
  localStorage.setItem("devices", JSON.stringify(devices));  
}  
  
// Rolle dieses Geräts  
let myRole = devices.find(d=>d.id===deviceID).role;  
console.log("Meine Rolle:", myRole);  
  
// Admin Controls nur wenn Rolle erlaubt  
if(myRole !== "add"){  
  document.getElementById("adminControls").style.display = "none";  
}  
  
// --- Speicher ---  
function save(){  
  localStorage.setItem("users", JSON.stringify(users));  
  localStorage.setItem("devices", JSON.stringify(devices));  
}  
  
// --- Funktionen ---  
function addUser(){  
  if(myRole !== "add") return alert("Nur das erste Gerät darf Punkte hinzufügen!");  
  const name = document.getElementById("nameInput").value;  
  if(!name) return;  
  users.push({name:name, points:0});  
  document.getElementById("nameInput").value = "";  
  save(); render();  
}  
  
function addPoint(index){  
  if(myRole !== "add") return alert("Nur das erste Gerät darf Punkte hinzufügen!");  
  users[index].points += 1;  
  save(); render();  
}  
  
function subtractMinutes(index){  
  if(myRole !== "subtract") return alert("Nur das zweite Gerät darf Minuten abziehen!");  
  const input = document.getElementById("input-"+index);  
  const error = document.getElementById("error-"+index);  
  
  let minutesToRemove = parseFloat(input.value);  
  if(!minutesToRemove || minutesToRemove <=0) return;  
  
  let currentMinutes = users[index].points*2;  
  
  if(minutesToRemove>currentMinutes){  
    error.textContent="Fehler: Zu viele Minuten eingegeben!";  
    return;  
  }  
  error.textContent="";  
  
  let newMinutes = currentMinutes - minutesToRemove;  
  users[index].points = newMinutes/2;  
  
  input.value="";  
  save(); render();  
}  
  
function resetUser(index){  
  if(myRole==="view") return alert("Nur die ersten 2 Geräte dürfen Aktionen ausführen!");  
  users[index].points=0;  
  save(); render();  
}  
  
// --- Render ---  
function render(){  
  const container = document.getElementById("users");  
  container.innerHTML="";  
  
  users.forEach((user,index)=>{  
    const minutes = user.points*2;  
    container.innerHTML += `  
      <div class="card">  
        <div class="name">${user.name}</div>  
        <div>⭐ Punkte: ${user.points}</div>  
        <div>⏱️ Minuten: ${minutes}</div>  
        ${myRole==="add"?`<button class="green" onclick="addPoint(${index})">+ Punkt</button>`:""}  
        ${myRole!=="view"?`<button class="red" onclick="resetUser(${index})">Reset</button>`:""}  
        <br><br>  
        ${myRole==="subtract"?`<input id="input-${index}" type="number" placeholder="Minuten">  
        <button class="orange" onclick="subtractMinutes(${index})">Abziehen</button>`:""}  
        <div id="error-${index}" class="error"></div>  
      </div>  
    `;  
  });  
}  
  
render();  
  
// Import the functions you need from the SDKs you need  
import { initializeApp } from "firebase/app";  
// TODO: Add SDKs for Firebase products that you want to use  
// https://firebase.google.com/docs/web/setup#available-libraries  
  
// Your web app's Firebase configuration  
const firebaseConfig = {  
  apiKey: "AIzaSyAGjv4a03o8gQFZ2XxjV--KG-Nnc58LLhw",  
  authDomain: "familienpunkte-cec1a.firebaseapp.com",  
  databaseURL: "https://familienpunkte-cec1a-default-rtdb.firebaseio.com",  
  projectId: "familienpunkte-cec1a",  
  storageBucket: "familienpunkte-cec1a.firebasestorage.app",  
  messagingSenderId: "648175206394",  
  appId: "1:648175206394:web:f07cd74f7a93d8708bae43"  
};  
  
// Initialize Firebase  
const app = initializeApp(firebaseConfig);  
  
const database = getDatabase(app);  
  
</script>  
  
</body>  
</html>  
