<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>今天吃点啥</title>
    <style>
        :root {
  --color-1: #8dbf8b;
  --color-2: #fcf1d8;
  --color-3: #fadc9c;
  --color-4: #f09e56;
}

body {
  background: linear-gradient(
    90deg,
    var(--color-1) 0%,
    var(--color-1) 25%,
    var(--color-2) 25%,
    var(--color-2) 50%,
    var(--color-3) 50%,
    var(--color-3) 75%,
    var(--color-4) 75%,
    var(--color-4) 100%
  );
}
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        h1 {
            color: #333;
            text-align: center;
        }
        #result {
            font-size: 1.5em;
            color: #d9534f;
            margin-top: 20px;
            padding: 10px 20px;
            border: 2px solid #d9534f;
            border-radius: 10px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        #refreshButton {
            margin-top: 20px;
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            background-color: #d9534f;
            color: #fff;
            font-size: 1em;
            cursor: pointer;
        }
        #refreshButton:hover {
            background-color: #c9302c;
        }
    </style>
    <script>
        function getRandomItem(array) {
            var randomIndex = Math.floor(Math.random() * array.length);
            return array[randomIndex];
        }

        var foodList = [
            "塔斯汀",
            "披萨",
            "关东煮",
            "炸鸡",
            "火锅",
            "烤肉饭",
            "v我50告诉你",
            "炒饭",
            "鱼粉",
            "卤肉饭",
            "馄饨",
            "黄焖鸡",
            "猪脚饭",
            "螺蛳粉",
            "饺子",
            "饭团",
            "烤鸡饭",
            "烤鸭饭",
            "热卤",
            "麻辣烫",
            "意面",
            "鸡公煲",
            "跟韩国人去吃泡菜",
            "小碗菜",
            "别炒，我在烧烤",
            "我也不r道啊",
            "鸡蛋灌饼",
            "铁板烧",
            "满汉全席（想得美）",
            "米线",
            "酸辣粉",
            "热干面",
            "梅菜扣肉饼",
            "KFC",
            "呱",
            "吃云南菌子",
            "冒菜",
            "叉烧饭",
            "煲仔饭",
            "泡面",
            "抢室友的饭",
            "外面啥都有",
            "串串",
            "肠粉",
            "蒸菜",
            "卷饼豆花",
            "go餐馆",
            "肉夹馍",
            "花甲粉",
            "麻辣香锅",
            "盖码饭",
            "过会吧，饿了就老实了",
            "换个学校"
        ];

        function selectRandomFood() {
            var randomFood = getRandomItem(foodList);
            document.getElementById("result").innerText = "今天的食物是: " + randomFood;
        }

        window.onload = function() {
            selectRandomFood();
        }
    </script>
</head>
<body>
    <h1>今天吃点啥</h1>
    <p id="result"></p >
    <button id="refreshButton" onclick="selectRandomFood()">我不</button>
</body>
</html>
