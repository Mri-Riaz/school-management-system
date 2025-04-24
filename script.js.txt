// Sample Data
let students = ['Alice', 'Bob', 'Charlie'];
let teachers = ['Mr. Smith', 'Ms. Johnson'];
let classes = ['Math 101', 'Science 101'];

// Update the Dashboard Stats
function updateDashboard() {
    document.getElementById('student-count').innerText = students.length;
    document.getElementById('teacher-count').innerText = teachers.length;
    document.getElementById('class-count').innerText = classes.length;
}

// Functions to Add New Data
function addStudent() {
    let name = prompt("Enter student's name:");
    if (name) {
        students.push(name);
        renderStudents();
        updateDashboard();
    }
}

function addTeacher() {
    let name = prompt("Enter teacher's name:");
    if (name) {
        teachers.push(name);
        renderTeachers();
        updateDashboard();
    }
}

function addClass() {
    let name = prompt("Enter class name:");
    if (name) {
        classes.push(name);
        renderClasses();
        updateDashboard();
    }
}

// Render Functions
function renderStudents() {
    let studentList = document.getElementById('student-list');
    studentList.innerHTML = students.map(student => `<p>${student}</p>`).join('');
}

function renderTeachers() {
    let teacherList = document.getElementById('teacher-list');
    teacherList.innerHTML = teachers.map(teacher => `<p>${teacher}</p>`).join('');
}

function renderClasses() {
    let classList = document.getElementById('class-list');
    classList.innerHTML = classes.map(cls => `<p>${cls}</p>`).join('');
}

// Attendance Function
function markAttendance() {
    let studentName = prompt("Enter student's name to mark attendance:");
    if (studentName) {
        alert(`${studentName}'s attendance has been marked!`);
    }
}

// Initial Rendering
updateDashboard();
renderStudents();
renderTeachers();
renderClasses();
