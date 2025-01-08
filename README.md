import React from 'react';
import{useState} from 'react';

import './App.css';

function App(){
  const[name,setName]=useState('');
  const[pass,setPassword]=useState('');

  const handleSubmit=(e)=>{
    e.preventDefault();//prevent page load
   if(name === "DARSHUU" && pass === "IMRD@123")
     {
    alert("Login Successful...");
   }
   else
   {
    alert("Login unsuccessful...");
   }
      
  };
  return (
    <div className="App">
    <h1>Login Form</h1>
      <form onSubmit={handleSubmit}> 
        <div>
          <label>Name - </label>
          <input type="text" value={name}
          onChange={(e)=> setName(e.target.value)}
          placeholder='enter your name...'></input>  
        </div>
        <div>
          <label>Password - </label>
          <input type="password" value={name}
          onChange={(e)=> setPassword(e.target.value)}
          placeholder='enter your email...'></input>  
        </div>
        <br></br>
        <div>
          <button type="submit">submit</button>
        </div>
        </form>
    
  </div>
  );
}

export default App;

