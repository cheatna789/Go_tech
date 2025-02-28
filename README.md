<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Money Verse - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to CSS file -->
    <script defer src="script.js"></script> <!-- Link to JavaScript file -->
</head>
<body>
    <header>
        <h1>Money Verse</h1>
        <p>Total Balance: <strong>$32,500.00</strong></p>
    </header>

    <section class="controls">
        <button class="toggle-btn active" id="expenses-btn">Expenses</button>
        <button class="toggle-btn" id="income-btn">Income</button>
        <select id="month-select">
            <option value="january">January</option>
            <option value="february">February</option>
            <option value="march">March</option>
            <option value="april">April</option>
            <option value="may">May</option>
            <option value="june" selected>June</option> <!-- Default -->
            <option value="july">July</option>
            <option value="august">August</option>
            <option value="september">September</option>
            <option value="october">October</option>
            <option value="november">November</option>
            <option value="december">December</option>
        </select>
    </section>

    <section id="expenses-graph">
        <h2>Expense Overview - <span id="selected-month">June</span></h2>
        <div class="graph">
            <div class="bar" style="height: 12%;" data-label="12%"></div>
            <div class="bar" style="height: 3%;" data-label="3%"></div>
            <div class="bar" style="height: 5%;" data-label="5%"></div>
            <div class="bar" style="height: 32%;" data-label="32%"></div>
            <div class="bar" style="height: 21%;" data-label="21%"></div>
            <div class="bar" style="height: 7%;" data-label="7%"></div>
            <div class="bar" style="height: 13%;" data-label="13%"></div>
            <div class="bar" style="height: 5%;" data-label="5%"></div>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Money Verse. All rights reserved.</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Money Verse - Budget Tracker</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://kit.fontawesome.com/your-fontawesome-kit.js" crossorigin="anonymous"></script>
</head>
<body>

    <!-- Header (Linked to Expense Tracker) -->
    <header>
        <h1>Money Verse</h1>
        <nav>
            <ul>
                <li><a href="#">Expenses</a></li>
                <li><a href="#">Budget</a></li>
                <li><a href="#">Rewards</a></li>
            </ul>
        </nav>
    </header>

    <!-- Monthly Budget Section -->
    <section class="budget-section">
        <h2>Monthly Budget</h2>
        <div class="month-selector">
            <i class="fa fa-calendar"></i>
            <select id="monthDropdown">
                <option>January 2025</option>
                <option>February 2025</option>
                <option>March 2025</option>
            </select>
        </div>

        <div class="budget-circle">
            <div class="progress-container">
                <svg>
                    <circle cx="50" cy="50" r="45"></circle>
                    <circle cx="50" cy="50" r="45" id="progressCircle"></circle>
                </svg>
                <span id="remainingAmount">$5,251</span>
            </div>
        </div>

        <div class="budget-categories">
            <div class="category">
                <div class="progress" data-percent="60"></div>
                <p>Housing</p>
            </div>
            <div class="category">
                <div class="progress" data-percent="20"></div>
                <p>Health</p>
            </div>
            <div class="category">
                <div class="progress" data-percent="15"></div>
                <p>Groceries</p>
            </div>
            <div class="category">
                <div class="progress" data-percent="8"></div>
                <p>Entertainment</p>
            </div>
            <div class="category">
                <div class="progress" data-percent="3"></div>
                <p>Other</p>
            </div>
        </div>
    </section>

    <!-- Rewards Section -->
    <section class="rewards-section">
        <h2>Rewards & Achievements</h2>
        <div class="reward">
            <i class="fa fa-star"></i>
            <p>Budget Master - Saved 20% of income</p>
        </div>
        <div class="reward">
            <i class="fa fa-medal"></i>
            <p>Expense Controller - Stayed under budget</p>
        </div>
        <div class="reward">
            <i class="fa fa-gift"></i>
            <p>Smart Saver - Invested in savings</p>
        </div>
    </section>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Savings Goal Tracker</title>
    <link rel="stylesheet" href="savings.css">
</head>
<body>

    <section class="savings-section">
        <h2>Savings Goals</h2>
        <div class="goal">
            <p>Vacation Fund</p>
            <progress id="goal1" value="500" max="1000"></progress>
            <span id="goal1-status">$500 / $1000</span>
            <button onclick="addSavings('goal1', 100)">+ $100</button>
        </div>

        <div class="goal">
            <p>Emergency Fund</p>
            <progress id="goal2" value="300" max="1500"></progress>
            <span id="goal2-status">$300 / $1500</span>
            <button onclick="addSavings('goal2', 200)">+ $200</button>
        </div>

        <div class="goal">
            <p>New Laptop</p>
            <progress id="goal3" value="700" max="1200"></progress>
            <span id="goal3-status">$700 / $1200</span>
            <button onclick="addSavings('goal3', 150)">+ $150</button>
        </div>
    </section>

    <script src="savings.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Leaderboard</title>
    <link rel="stylesheet" href="leaderboard.css">
</head>
<body>

    <section class="leaderboard-section">
        <h2>Top Savers</h2>
        <table>
            <thead>
                <tr>
                    <th>Rank</th>
                    <th>Name</th>
                    <th>Savings</th>
                </tr>
            </thead>
            <tbody id="leaderboard">
                <tr>
                    <td>1</td>
                    <td>Alice</td>
                    <td>$3,500</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Bob</td>
                    <td>$2,900</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>Charlie</td>
                    <td>$2,500</td>
                </tr>
            </tbody>
        </table>
    </section>

    <script src="leaderboard.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Savings Goal Tracker</title>
    <link rel="stylesheet" href="savings.css">
</head>
<body>

    <section class="savings-section">
        <h2>Savings Goals</h2>
        <div class="goal">
            <p>Vacation Fund</p>
            <progress id="goal1" value="500" max="1000"></progress>
            <span id="goal1-status">$500 / $1000</span>
            <button onclick="addSavings('goal1', 100)">+ $100</button>
        </div>

        <div class="goal">
            <p>Emergency Fund</p>
            <progress id="goal2" value="300" max="1500"></progress>
            <span id="goal2-status">$300 / $1500</span>
            <button onclick="addSavings('goal2', 200)">+ $200</button>
        </div>

        <div class="goal">
            <p>New Laptop</p>
            <progress id="goal3" value="700" max="1200"></progress>
            <span id="goal3-status">$700 / $1200</span>
            <button onclick="addSavings('goal3', 150)">+ $150</button>
        </div>
    </section>

    <script src="savings.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Savings Tracker</title>
    <link rel="stylesheet" href="savings.css">
</head>
<body>
    <section class="savings">
        <h2>Savings Goals</h2>
        <div class="goal">
            <p>Vacation Fund</p>
            <progress id="goal1" value="500" max="1000"></progress>
            <button onclick="addSavings('goal1', 100)">+ $100</button>
        </div>
        <div class="goal">
            <p>Emergency Fund</p>
            <progress id="goal2" value="300" max="1500"></progress>
            <button onclick="addSavings('goal2', 200)">+ $200</button>
        </div>
    </section>
    <script src="savings.js"></script>
</body>
</html>
<nav>
    <a href="savings.html">Savings</a>
    <a href="leaderboard.html">Leaderboard</a>
</nav>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f9f9f9;
    margin: 0;
    padding: 0;
}

header {
    background: #fff;
    padding: 20px;
    box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
}

.controls {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 20px;
    gap: 10px;
}

.toggle-btn {
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    font-size: 16px;
    border-radius: 20px;
    transition: 0.3s;
}

.toggle-btn.active {
    background: black;
    color: white;
}

select {
    padding: 10px;
    font-size: 16px;
    border-radius: 10px;
}

#expenses-graph {
    max-width: 500px;
    margin: auto;
}

.graph {
    display: flex;
    justify-content: space-around;
    align-items: flex-end;
    height: 200px;
    margin-top: 20px;
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
}

.bar {
    width: 30px;
    background: #6a5acd;
    position: relative;
    border-radius: 5px;
}

.bar::after {
    content: attr(data-label);
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 12px;
    color: #333;
}
/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #f8f9fa;
}

header {
    background: #1e1e2d;
    color: white;
    padding: 15px;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

/* Budget Section */
.budget-section {
    text-align: center;
    padding: 20px;
}

.month-selector {
    background: white;
    display: inline-flex;
    align-items: center;
    padding: 10px;
    border-radius: 10px;
}

.month-selector i {
    margin-right: 10px;
}

.budget-circle {
    display: flex;
    justify-content: center;
    margin-top: 20px;
}

.progress-container {
    position: relative;
    width: 100px;
    height: 100px;
}

svg {
    width: 100px;
    height: 100px;
}

circle {
    fill: none;
    stroke: lightgray;
    stroke-width: 10;
}

#progressCircle {
    stroke: green;
    stroke-dasharray: 283;
    stroke-dashoffset: 85;
    stroke-linecap: round;
    transition: stroke-dashoffset 1s ease;
}

#remainingAmount {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 18px;
    font-weight: bold;
}

/* Budget Categories */
.budget-categories {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 20px;
}

.category {
    text-align: center;
}

.progress {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: conic-gradient(
        green 0% 0%, 
        lightgray 0% 100%
    );
}

/* Rewards Section */
.rewards-section {
    text-align: center;
    padding: 20px;
    background: white;
    margin-top: 30px;
}

.reward {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    padding: 10px;
    border-radius: 5px;
    background: #e9ecef;
    margin: 10px auto;
    width: 80%;
}

.reward i {
    font-size: 24px;
    color: gold;
}
body {
    font-family: Arial, sans-serif;
    background: #f8f9fa;
    padding: 20px;
}

.savings-section {
    text-align: center;
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 80%;
    margin: auto;
}

.goal {
    margin: 20px 0;
}

progress {
    width: 80%;
    height: 20px;
    appearance: none;
}

progress[value]::-webkit-progress-bar {
    background: lightgray;
    border-radius: 10px;
}

progress[value]::-webkit-progress-value {
    background: green;
    border-radius: 10px;
}

button {
    padding: 8px 12px;
    margin-top: 10px;
    border: none;
    background: #28a745;
    color: white;
    cursor: pointer;
}
body {
    font-family: Arial, sans-serif;
    background: #f8f9fa;
    padding: 20px;
}

.leaderboard-section {
    text-align: center;
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 80%;
    margin: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: center;
}

th {
    background: #007bff;
    color: white;
}

td {
    background: #f8f9fa;
}
body {
    font-family: Arial, sans-serif;
    background: #f8f9fa;
    padding: 20px;
}

.savings-section {
    text-align: center;
    background: white;
    padding: 20px;
    border-radius: 10px;
    width: 80%;
    margin: auto;
}

.goal {
    margin: 20px 0;
}

progress {
    width: 80%;
    height: 20px;
    appearance: none;
}

progress[value]::-webkit-progress-bar {
    background: lightgray;
    border-radius: 10px;
}

progress[value]::-webkit-progress-value {
    background: green;
    border-radius: 10px;
}

button {
    padding: 8px 12px;
    margin-top: 10px;
    border: none;
    background: #28a745;
    color: white;
    cursor: pointer;
}
body { font-family: Arial, sans-serif; background: #f8f9fa; text-align: center; }
.savings { background: white; padding: 20px; border-radius: 10px; width: 80%; margin: auto; }
progress { width: 80%; height: 20px; }
button { padding: 8px 12px; border: none; background: green; color: white; cursor: pointer; }
document.addEventListener("DOMContentLoaded", function () {
    const monthSelect = document.getElementById("month-select");
    const selectedMonth = document.getElementById("selected-month");

    // Example: Expense Data for Each Month
    const expenseData = {
        january: [10, 5, 8, 20, 15, 7, 10, 5],
        february: [5, 3, 6, 18, 12, 6, 8, 4],
        march: [15, 10, 12, 25, 20, 10, 12, 6],
        april: [8, 4, 5, 15, 10, 5, 8, 3],
        may: [12, 6, 7, 22, 17, 8, 10, 5],
        june: [12, 3, 5, 32, 21, 7, 13, 5], // Default
        july: [14, 6, 9, 28, 18, 9, 11, 7],
        august: [11, 5, 6, 23, 16, 8, 9, 4],
        september: [9, 4, 5, 18, 12, 6, 7, 3],
        october: [13, 6, 8, 27, 19, 9, 11, 6],
        november: [10, 5, 7, 20, 15, 8, 10, 4],
        december: [8, 3, 5, 15, 10, 6, 9, 2]
    };

    // Function to Update the Graph Based on Selected Month
    function updateGraph(month) {
        selectedMonth.textContent = month.charAt(0).toUpperCase() + month.slice(1); // Capitalize month name

        const bars = document.querySelectorAll(".bar");
 // Dynamic leaderboard with random values (for simulation)
document.addEventListener("DOMContentLoaded", function() {
    const leaderboardData = [
        { name: "Alice", savings: Math.floor(Math.random() * 5000) },
        { name: "Bob", savings: Math.floor(Math.random() * 5000) },
        { name: "Charlie", savings: Math.floor(Math.random() * 5000) },
        { name: "Dave", savings: Math.floor(Math.random() * 5000) },
        { name: "Eve", savings: Math.floor(Math.random() * 5000) }
    ];

    // Sort leaderboard data by savings (descending)
    leaderboardData.sort((a, b) => b.savings - a.savings);

    let tableBody = document.getElementById("leaderboard");
    tableBody.innerHTML = ""; // Clear existing rows

    leaderboardData.forEach((user, index) => {
        let row = `<tr>
            <td>${index + 1}</td>
            <td>${user.name}</td>
            <td>$${user.savings}</td>
        </tr>`;
        tableBody.innerHTML += row;
    });
});       const data = expenseData[month];

        bars.forEach((bar, index) => {
            bar.style.height = data[index] + "%";
            bar.setAttribute("data-label", data[index] + "%");
        });
    }

    // Listen for Month Change
    monthSelect.addEventListener("change", function () {
        updateGraph(this.value);
    });

    // Initial Load (June by default)
    updatedocument.addEventListener("DOMContentLoaded", function() {
    const progressCircle = document.getElementById("progressCircle");
    const remainingAmount = document.getElementById("remainingAmount");

    // Budget data for different months
    const budgetData = {
        "January 2025": { remaining: "$5,251", progress: 85 },
        "February 2025": { remaining: "$4,800", progress: 120 },
        "March 2025": { remaining: "$3,600", progress: 160 }
    };

    // Update UI when the month changes
    document.getElementById("monthDropdown").addEventListener("change", function() {
        let selectedMonth = this.value;
        remainingAmount.innerText = budgetData[selectedMonth].remaining;
        progressCircle.style.strokeDashoffset = budgetData[selectedMonth].progress;
    });

    // Dynamic Circular Progress for Budget Categories
    document.querySelectorAll(".progress").forEach(progress => {
        let percent = progress.dataset.percent;
        progress.style.background = `conic-gradient(
            green 0% ${percent}%, 
            lightgray ${percent}% 100%
        )`;
    });
});Graph("june");
});
// Dynamic leaderboard with random values (for simulation)
document.addEventListener("DOMContentLoaded", function() {
    const leaderboardData = [
        { name: "Alice", savings: Math.floor(Math.random() * 5000) },
        { name: "Bob", savings: Math.floor(Math.random() * 5000) },
        { name: "Charlie", savings: Math.floor(Math.random() * 5000) },
        { name: "Dave", savings: Math.floor(Math.random() * 5000) },
        { name: "Eve", savings: Math.floor(Math.random() * 5000) }
    ];

    // Sort leaderboard data by savings (descending)
    leaderboardData.sort((a, b) => b.savings - a.savings);

    let tableBody = document.getElementById("leaderboard");
    tableBody.innerHTML = ""; // Clear existing rows

    leaderboardData.forEach((user, index) => {
        let row = `<tr>
            <td>${index + 1}</td>
            <td>${user.name}</td>
            <td>$${user.savings}</td>
        </tr>`;
        tableBody.innerHTML += row;
    });
});
function addSavings(goalId, amount) {
    let goal = document.getElementById(goalId);
    let currentSavings = parseInt(goal.value);
    let maxSavings = parseInt(goal.max);

    if (currentSavings + amount <= maxSavings) {
        goal.value = currentSavings + amount;
        document.getElementById(goalId + "-status").innerText = $${goal.value} / $${maxSavings};
    } else {
        alert("Goal already reached!");
    }
}

