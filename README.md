# Loginform-React

//import logo from './logo.svg';

import React from 'react';
import{useState} from 'react';
const App=()=>{
  const[name,setName]=useState('');
  const[email,setEmail]=useState('');

  const handleSubmit=(e)=>{
    e.preventDefault();
    alert(`form Submitted with : \nname: ${name} \nemail: ${email}`
      );
  };
  return (
    <div>
    <h1>
      simple web form</h1>
      <form name="f1" onSubmit={handleSubmit}> 

        <div>
          <label>name</label>
          <input type="text" value={name}
          onChange={(e)=> setName(e.target.value)}
          placeholder="enter your name"
          
          ></input>  
        </div>
        <div>
          <label>email</label>
          <input type="email" value={email}
          onChange={(e)=> setEmail(e.target.value)}
          placeholder="enter your email"
          
          ></input>  
        </div>
        <div>
          <button type="submit">submit</button>
        </div>
        

      </form>
    
  </div>
  );
}

export default App;
