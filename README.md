<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>永久地址導航</title>
    <style>
        body { background: #121212; color: #ffffff; font-family: "Microsoft JhengHei", sans-serif; text-align: center; padding-top: 50px; }
        .box { max-width: 400px; margin: 0 auto; padding: 20px; }
        .btn { 
            display: block; background: #333; color: #f39c12; 
            padding: 15px; margin-bottom: 20px; text-decoration: none; 
            border-radius: 8px; border: 1px solid #444; font-weight: bold;
        }
        .btn:hover { background: #444; border-color: #f39c12; }
        .tip { color: #666; font-size: 12px; margin-top: 50px; }
    </style>
</head>
<body>
    <div class="box">
        <h2 style="color:#f39c12">最新訪問網址</h2>
        
        <a href="#" class="btn" data-url="https://m1fuping.lol" onclick="go(this)">最新網址 (1) - 點擊進入</a>
        <a href="#" class="btn" data-url="https://rapidtai.com" onclick="go(this)">最新網址 (2) - 點擊進入</a>
        <a href="#" class="btn" data-url="https://taimadou.com" onclick="go(this)">最新網址 (3) - 點擊進入</a>
        
        <div class="tip">
            建議收藏本頁面，地址失效請返回此處
        </div>
    </div>

    <script>
        function go(obj) {
            // 获取 data-url 属性并跳转
            var url = obj.getAttribute('data-url');
            window.location.href = url;
        }
    </script>
</body>
</html>
