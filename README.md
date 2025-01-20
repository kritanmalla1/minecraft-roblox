// script.js

// Theme Switcher
const themeToggle = document.getElementById('themeToggle');
const body = document.body;

themeToggle.addEventListener('click', () => {
  body.classList.toggle('dark-mode');
  if (body.classList.contains('dark-mode')) {
    themeToggle.textContent = 'Switch to Light Mode';
  } else {
    themeToggle.textContent = 'Switch to Dark Mode';
  }
});

// To-Do List
const todoInput = document.getElementById('todo-input');
const addTaskButton = document.getElementById('add-task');
const todoItems = document.getElementById('todo-items');

addTaskButton.addEventListener('click', () => {
  if (todoInput.value.trim()) {
    const li = document.createElement('li');
    li.textContent = todoInput.value.trim();
    todoItems.appendChild(li);
    todoInput.value = ''; // Clear input
  }
});

// GPA Calculator
const gradeInput = document.getElementById('course-grade');
const addGradeButton = document.getElementById('add-grade');
const gpaResult = document.getElementById('gpa-result');

let grades = [];

addGradeButton.addEventListener('click', () => {
  const grade = parseFloat(gradeInput.value);
  if (!isNaN(grade) && grade >= 0 && grade <= 4) {
    grades.push(grade);
    const gpa = (grades.reduce((a, b) => a + b, 0) / grades.length).toFixed(2);
    gpaResult.textContent = `Your GPA: ${gpa}`;
    gradeInput.value = ''; // Clear input
  } else {
    alert('Please enter a valid grade between 0 and 4.');
  }
});
