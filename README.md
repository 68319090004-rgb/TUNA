<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Water Pump Dashboard</title>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Kanit', sans-serif;
            background-color: #f8f0ff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .container {
            width: 90%;
            max-width: 600px;
            background-color: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            text-align: center;
        }

        /* ส่วนหัวเรื่อง */
        .header {
            background-color: #92e3e2;
            padding: 15px;
            border-radius: 50px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed #444;
            margin-bottom: 30px;
            padding-left: 40px;
            padding-right: 40px;
        }

        .header h1 {
            margin: 0;
            font-size: 24px;
            color: #333;
        }

        .header-icon {
            font-size: 30px;
            margin-left: 10px;
        }

        /* แถบสถานะต่างๆ */
        .status-bar {
            display: flex;
            align-items: center;
            padding: 15px 25px;
            margin-bottom: 15px;
            border-radius: 15px;
            color: black;
            font-size: 20px;
            font-weight: 500;
        }

        .icon {
            width: 40px;
            margin-right: 15px;
            text-align: center;
        }

        .moisture { background-color: #e2b6f3; width: 80%; }
        .pump { background-color: #8ce366; width: 90%; }
        .mode { background-color: #00bcd4; width: 100%; color: black; }

        .value-right {
            margin-left: auto;
        }

        /* ส่วนของปุ่ม Switch */
        .controls {
            display: flex;
            justify-content: space-around;
            margin-top: 40px;
        }

        .switch-group {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .switch-label {
            font-size: 18px;
            margin-bottom: 10px;
        }

        .toggle {
            position: relative;
            width: 120px;
            height: 50px;
            background: linear-gradient(to right, #a066ff, #66e0ff);
            border-radius: 50px;
            display: flex;
            align-items: center;
            padding: 5px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .toggle-circle {
            width: 40px;
            height: 40px;
            background: linear-gradient(to bottom, #4facfe 0%, #00f2fe 100%);
            border-radius: 50%;
            position: absolute;
            left: 5px;
            transition: 0.3s;
        }

        .toggle-text {
            width: 100%;
            text-align: right;
            padding-right: 15px;
            font-weight: bold;
            font-size: 22px;
            color: #444;
        }

        .sub-label {
            font-size: 12px;
            color: #666;
            margin-top: 5px;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="header">
            <h1>Smart Water Pump</h1>
            <span class="header-icon">🌲</span>
        </div>

        <div class="status-bar moisture">
            <div class="icon">💧</div>
            <span>ค่าความชื้น</span>
            <span class="value-right">%</span>
        </div>

        <div class="status-bar pump">
            <div class="icon">⚙️</div>
            <span>สถานะปั๊ม</span>
        </div>

        <div class="status-bar mode">
            <div class="icon">⚙️</div>
            <span>โหมด</span>
        </div>

        <div class="controls">
            <div class="switch-group">
                <div class="switch-label">ระบบ</div>
                <div class="toggle">
                    <div class="toggle-circle"></div>
                    <div class="toggle-text">ON</div>
                </div>
                <div class="sub-label">on / off</div>
            </div>

            <div class="switch-group">
                <div class="switch-label">โหมด Auto</div>
                <div class="toggle">
                    <div class="toggle-circle"></div>
                    <div class="toggle-text">ON</div>
                </div>
                <div class="sub-label">on / off</div>
            </div>
        </div>
    </div>

</body>
</html>
