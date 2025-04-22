<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Food Outlet Sales Data Visualization</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5em;
            color: #4CAF50;
        }

        section {
            margin-bottom: 50px;
        }

        .card {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin: 10px;
            display: inline-block;
            width: 280px;
            text-align: center;
        }

        .card h2 {
            color: #333;
        }

        .card p {
            font-size: 1.2em;
            margin: 10px 0;
        }

        .card .value {
            font-size: 1.5em;
            font-weight: bold;
            color: #4CAF50;
        }

        .chart-container {
            display: flex;
            justify-content: space-around;
            margin-top: 40px;
        }

        .chart-container canvas {
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        footer {
            text-align: center;
            font-size: 0.9em;
            color: #777;
            margin-top: 50px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Food Outlet Sales Data Visualization</h1>
        <p>A comprehensive dashboard displaying key sales metrics for a food outlet</p>
    </header>

    <section>
        <div class="card">
            <h2>Total MRP of Items</h2>
            <p class="value">$4500</p>
        </div>
        <div class="card">
            <h2>Total Weight of Items</h2>
            <p class="value">350 kg</p>
        </div>
        <div class="card">
            <h2>Total Outlets</h2>
            <p class="value">12</p>
        </div>
    </section>

    <section class="chart-container">
        <div>
            <h3>Pie Chart: Tier Distribution</h3>
            <!-- Include your pie chart library here -->
            <canvas id="pieChart" width="300" height="300"></canvas>
        </div>
        <div>
            <h3>Donut Chart: Fat Distribution</h3>
            <!-- Include your donut chart library here -->
            <canvas id="donutChart" width="300" height="300"></canvas>
        </div>
        <div>
            <h3>Bar Chart: Total MRP of Food Items</h3>
            <!-- Include your bar chart library here -->
            <canvas id="barChart" width="300" height="300"></canvas>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Food Outlet Analytics. All Rights Reserved.</p>
    </footer>

    <!-- Add your JavaScript for charts here -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script>
        // Pie chart for Tier Distribution
        var pieChart = new Chart(document.getElementById('pieChart'), {
            type: 'pie',
            data: {
                labels: ['Tier 1', 'Tier 2', 'Tier 3'],
                datasets: [{
                    data: [50, 30, 20],
                    backgroundColor: ['#ff6666', '#ffcc66', '#66ff66'],
                }]
            }
        });

        // Donut chart for Fat Distribution
        var donutChart = new Chart(document.getElementById('donutChart'), {
            type: 'doughnut',
            data: {
                labels: ['Low Fat', 'Medium Fat', 'High Fat'],
                datasets: [{
                    data: [40, 30, 30],
                    backgroundColor: ['#4CAF50', '#FFC107', '#F44336'],
                }]
            }
        });

        // Bar chart for Total MRP of Food Items
        var barChart = new Chart(document.getElementById('barChart'), {
            type: 'bar',
            data: {
                labels: ['Item 1', 'Item 2', 'Item 3', 'Item 4'],
                datasets: [{
                    label: 'Total MRP',
                    data: [500, 800, 1200, 1000],
                    backgroundColor: '#4CAF50',
                }]
            }
        });
    </script>
</body>
</html>
