# Debugging Assistant Prompt

## Purpose
This prompt helps you debug complex issues in your code by leveraging Trae IDE's AI capabilities to analyze problems and suggest solutions.

## Prompt Template

```
You are Trae AI, a powerful agentic AI coding assistant. I'm experiencing an issue with my [LANGUAGE/FRAMEWORK] project. Please help me debug the following problem:

**Error Message/Symptom:**
[ERROR_MESSAGE]

**Relevant Code:**
```[LANGUAGE]
[CODE_SNIPPET]
```

**Expected Behavior:**
[EXPECTED_BEHAVIOR]

**What I've Tried:**
[ATTEMPTED_SOLUTIONS]

Please analyze the issue, identify potential causes, and suggest solutions. If you need to see more code or context, please let me know.
```

## Usage Instructions

1. Replace `[LANGUAGE/FRAMEWORK]` with your programming language or framework (e.g., JavaScript, React, Python)
2. Replace `[ERROR_MESSAGE]` with the exact error message or description of symptoms
3. Replace `[LANGUAGE]` with the language of your code snippet for proper syntax highlighting
4. Replace `[CODE_SNIPPET]` with the relevant code where the issue occurs
5. Replace `[EXPECTED_BEHAVIOR]` with what you expect the code to do
6. Replace `[ATTEMPTED_SOLUTIONS]` with what you've already tried to fix the issue
7. Copy the modified prompt into Trae IDE
8. Let Trae analyze and suggest solutions

## Example

```
You are Trae AI, a powerful agentic AI coding assistant. I'm experiencing an issue with my React project. Please help me debug the following problem:

**Error Message/Symptom:**
Uncaught TypeError: Cannot read property 'map' of undefined

**Relevant Code:**
```jsx
import React, { useState, useEffect } from 'react';

function UserList() {
  const [users, setUsers] = useState();
  
  useEffect(() => {
    fetch('https://api.example.com/users')
      .then(response => response.json())
      .then(data => setUsers(data));
  }, []);
  
  return (
    <div>
      <h2>User List</h2>
      <ul>
        {users.map(user => (
          <li key={user.id}>{user.name}</li>
        ))}
      </ul>
    </div>
  );
}

export default UserList;
```

**Expected Behavior:**
The component should display a list of users fetched from the API.

**What I've Tried:**
I've checked the API endpoint and it returns data correctly when tested in Postman.

Please analyze the issue, identify potential causes, and suggest solutions. If you need to see more code or context, please let me know.
```