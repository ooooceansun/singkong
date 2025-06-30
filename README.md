<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>星空纪民谣音乐酒馆 - 每日抽奖活动</title>
    <style>
        body {
            font-family: 'Microsoft YaHei', sans-serif;
            background-color: #1a1a2e;
            color: #fff;
            margin: 0;
            padding: 0;
            background-image: url('2c1a24c3-ae81-4a2d-856b-4ddd8b0633bd.png');
            background-size: cover;
            background-position: center;
        }
        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.1);
        }
        h1 {
            text-align: center;
            color: #f8c537;
            margin-bottom: 30px;
        }
        .prize {
            text-align: center;
            font-size: 24px;
            margin-bottom: 10px;
            color: #f8c537;
        }
        .prize-image {
            text-align: center;
            margin-bottom: 30px;
        }
        .prize-image img {
            max-width: 100%;
            border-radius: 10px;
        }
        .time {
            text-align: center;
            font-size: 18px;
            margin-bottom: 30px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input {
            width: 100%;
            padding: 10px;
            border-radius: 5px;
            border: none;
            background-color: rgba(255, 255, 255, 0.9);
        }
        button {
            background-color: #f8c537;
            color: #000;
            border: none;
            padding: 12px 30px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            display: block;
            margin: 0 auto;
            transition: all 0.3s;
        }
        button:hover {
            background-color: #ffd700;
            transform: scale(1.05);
        }
        .rules {
            margin-top: 30px;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
        }
        footer {
            text-align: center;
            margin-top: 30px;
            font-size: 14px;
            color: #aaa;
        }
        .error {
            color: #ff6b6b;
            text-align: center;
            margin: 10px 0;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>星空纪民谣音乐酒馆</h1>
        <div class="prize">每日抽奖：价值198元豪华威士忌套餐</div>
        <div class="prize-image">
            <img src="62b32c46-fba5-4249-89d8-f4cd9b0e6826.jpg" alt="豪华威士忌套餐">
        </div>
        <div class="time">每日开奖时间：下午5点 · 每日20位幸运顾客</div>
        
        <form id="lotteryForm">
            <div class="form-group">
                <label for="name">您的姓名：</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="phone">联系电话：</label>
                <input type="tel" id="phone" name="phone" required>
            </div>
            
            <div class="error" id="error"></div>
            
            <button type="submit">立即参与抽奖</button>
        </form>
        
        <div class="rules">
            <h3>活动规则：</h3>
            <ul>
                <li>每日抽奖一次，开奖时间为下午5点</li>
                <li>每日产生20位幸运顾客</li>
                <li>中奖者将收到当场提示</li>
                <li>奖品为价值198元豪华威士忌套餐</li>
                <li>中奖后请在3天内到店领取</li>
                <li>每人每天限参与一次</li>
            </ul>
        </div>
        
        <footer>
            © 2023 星空纪民谣音乐酒馆 保留所有权利
        </footer>
    </div>

    <script>
        document.getElementById('lotteryForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('name').value.trim();
            const phone = document.getElementById('phone').value.trim();
            const errorElement = document.getElementById('error');

            errorElement.style.display = 'none';

            if (!name || !phone) {
                errorElement.textContent = '姓名和电话不能为空';
                errorElement.style.display = 'block';
                return;
            }

            if (!/^1[3-9]\\d{9}$/.test(phone)) {
                errorElement.textContent = '请输入有效的手机号码';
                errorElement.style.display = 'block';
                return;
            }

            const isWinner = Math.random() < 0.2; // 20% 概率中奖
            if (isWinner) {
                alert('🎉 恭喜您中奖啦！请向工作人员出示此页面并领取价值198元的豪华威士忌套餐！');
            } else {
                alert('很遗憾，您未中奖，欢迎明日再来参与！');
            }

            document.getElementById('lotteryForm').reset();
        });
    </script>
</body>
</html>
