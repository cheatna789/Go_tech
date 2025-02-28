<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Expense Tracker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #F8FAFC;
            margin: 0;
            padding: 20px;
            text-align: center;
        }

        .container {
            max-width: 400px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .balance {
            font-size: 24px;
            font-weight: bold;
        }

        .toggle-buttons {
            display: flex;
            justify-content: center;
            margin: 20px 0;
        }

        .toggle-buttons button {
            flex: 1;
            padding: 10px;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        .active {
            background: black;
            color: white;
            border-radius: 20px;
        }

        .bar-chart {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            height: 150px;
            margin: 20px 0;
        }

        .bar {
            width: 30px;
            background: #ddd;
            text-align: center;
            border-radius: 5px;
            color: black;
        }

        .bar.green { background: #A8F0B0; }
        .bar.blue { background: #A0D8FF; }
        .bar.yellow { background: #FFE490; }
        .bar.purple { background: #C8B6FF; }
        .bar.pink { background: #FDCFE8; }

        .summary {
            display: flex;
            justify-content: space-around;
            margin: 20px 0;
        }

        .summary div {
            background: #EEE;
            padding: 10px;
            border-radius: 10px;
            text-align: center;
        }

        .expense-list {
            text-align: left;
            padding: 10px;
        }

        .expense-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            border-bottom: 1px solid #EEE;
        }

        .icon {
            display: flex;
            align-items: center;
        }

        .icon span {
            margin-left: 10px;
        }
    </style>
</head>
<body>

    <div class="container">
        <p class="balance">$32,500.00</p>
        <p>Total Balance</p>

        <div class="toggle-buttons">
            <button class="active">Expenses</button>
            <button>Income</button>
            <button>June ▼</button>
        </div>

        <div class="bar-chart">
            <div class="bar pink" style="height: 50px;">12%</div>
            <div class="bar blue" style="height: 20px;">3%</div>
            <div class="bar yellow" style="height: 30px;">5%</div>
            <div class="bar green" style="height: 100px;">32%</div>
            <div class="bar purple" style="height: 80px;">21%</div>
            <div class="bar blue" style="height: 40px;">7%</div>
            <div class="bar pink" style="height: 60px;">13%</div>
            <div class="bar yellow" style="height: 30px;">5%</div>
        </div>

        <div class="summary">
            <div>
                <p>Day</p>
                <p>$52</p>
            </div>
            <div>
                <p>Week</p>
                <p>$403</p>
            </div>
            <div>
                <p>Month</p>
                <p>$1,612</p>
            </div>
        </div>

        <div class="expense-list">
            <div class="expense-item">
                <div class="icon">
                    <span>👕</span>
                    <span>Shopping</span>
                </div>
                <span>$498.50</span>
            </div>
            <div class="expense-item">
                <div class="icon">
                    <span>🎁</span>
                    <span>Gifts</span>
                </div>
                <span>$344.45</span>
            </div>
            <div class="expense-item">
                <div class="icon">
                    <span>🍕</span>
                    <span>Food</span>
                </div>
                <span>$230.50</span>
            </div>
        </div>
    </div>

</body>
</html>
