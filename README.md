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
