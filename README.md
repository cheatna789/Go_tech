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

