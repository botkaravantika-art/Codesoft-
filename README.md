# Codesoft-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Online Quiz Maker</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="quiz-container">
    <h2 class="question-count">Question 1/3</h2>
    <h1 class="question">
        Have you practiced sport or any physical activity
        out of your working hours at least 30 min or more
        during the last month?
    </h1>

    <div class="options">
        <button class="option">3 times or more per week</button>
        <button class="option">1 or 2 times per week</button>
        <button class="option">Less than 4 times per month</button>
        <button class="option">I don't practice sport during the month</button>
    </div>

    <button id="nextBtn">Next Question</button>
</div>

<script src="script.js"></script>
</body>
</html>

style.css
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #9ff3ef, #6ec6ca);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.quiz-container {
    background: #e8ffff;
    width: 90%;
    max-width: 600px;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    text-align: center;
}

.question-count {
    color: #555;
    font-size: 14px;
}

.question {
    font-size: 18px;
    margin: 20px 0;
}

.options {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.option {
    padding: 15px;
    border-radius: 25px;
    border: none;
    font-size: 15px;
    cursor: pointer;
    background: white;
    transition: 0.3s;
}

.option:hover {
    background: #3ac7c7;
    color: white;
}

.option.selected {
    background: #2bb3b3;
    color: white;
}

#nextBtn {
    margin-top: 20px;
    padding: 12px 25px;
    background: #2bb3b3;
    color: white;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
}

#nextBtn:hover {
    background: #239999;
}

script.js 
const options = document.querySelectorAll(".option");
const nextBtn = document.getElementById("nextBtn");

let selectedOption = null;

options.forEach(option => {
    option.addEventListener("click", () => {
        options.forEach(opt => opt.classList.remove("selected"));
        option.classList.add("selected");
        selectedOption = option.innerText;
    });
});

nextBtn.addEventListener("click", () => {
    if (selectedOption === null) {
        alert("Please select an option");
    } else {
        alert("Answer submitted: " + selectedOption);
        // next question logic can be added here
    }
});

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Job Board</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- Navbar -->
<header class="navbar">
  <div class="logo">🔍 Job Board</div>
  <nav>
    <a href="#">Home</a>
    <a href="#">Browse Jobs</a>
    <a href="#">Pages</a>
    <a href="#">Blog</a>
    <a href="#">Contact</a>
  </nav>
  <div class="nav-btns">
    <button class="login">Log in</button>
    <button class="post">Post a Job</button>
  </div>
</header>

<!-- Hero Section -->
<section class="hero">
  <div class="hero-text">
    <p class="count">4536+ Jobs listed</p>
    <h1>Find your Dream Job</h1>
    <p class="subtitle">
      We provide online instant cash loans with quick approval that suit your term length
    </p>
    <button class="upload">Upload Your Resume</button>
  </div>

  <div class="hero-image">
    <img src="https://i.imgur.com/0Z8FQ8G.png" alt="Job Illustration">
  </div>
</section>

<!-- Search Bar -->
<section class="search">
  <input type="text" placeholder="Search keyword">
  <input type="text" placeholder="Location">
  <select>
    <option>Category</option>
    <option>IT</option>
    <option>Finance</option>
    <option>Marketing</option>
  </select>
  <button>Find Job</button>
</section>

</body>
</html>
style.css 
* {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  box-sizing: border-box;
}

/* Navbar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 60px;
  background: #1e88e5;
  color: white;
}

.navbar nav a {
  margin: 0 12px;
  color: white;
  text-decoration: none;
}

.nav-btns button {
  margin-left: 10px;
  padding: 8px 14px;
  border: none;
  cursor: pointer;
}

.login {
  background: transparent;
  color: white;
}

.post {
  background: #2ecc71;
  color: white;
  border-radius: 4px;
}

/* Hero */
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 60px;
  background: linear-gradient(135deg, #1e88e5, #42a5f5);
  color: white;
}

.hero-text {
  max-width: 500px;
}

.count {
  font-size: 18px;
  margin-bottom: 10px;
}

.hero h1 {
  font-size: 42px;
  margin-bottom: 15px;
}

.subtitle {
  margin-bottom: 20px;
}

.upload {
  padding: 12px 20px;
  background: #2ecc71;
  border: none;
  color: white;
  border-radius: 4px;
  font-size: 16px;
}

.hero-image img {
  width: 350px;
}

/* Search */
.search {
  display: flex;
  gap: 10px;
  padding: 20px 60px;
  background: #f5f5f5;
}

.search input,
.search select {
  padding: 10px;
  flex: 1;
}

.search button {
  background: #2ecc71;
  color: white;
  border: none;
  padding: 10px 20px;
}
