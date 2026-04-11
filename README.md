<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>永久發佈頁 - 穩定訪問地址</title>
    <style>
        body { background: #1a1a1a; color: #eee; font-family: -apple-system, sans-serif; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0; }
        .container { width: 90%; max-width: 500px; text-align: center; }
        h1 { color: #f39c12; font-size: 1.5rem; margin-bottom: 30px; }
        .card { background: #2c3e50; border-radius: 12px; padding: 20px; margin-bottom: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.3); transition: transform 0.2s; cursor: pointer; display: block; text-decoration: none; color: white; }
        .card:hover { transform: translateY(-5px); background: #34495e; border: 1px solid #f39c12; }
        .card h2 { margin: 0; font-size: 1.1rem; color: #f39c12; }
        .card p { margin: 10px 0 0; font-size: 0.9rem; opacity: 0.8; }
        .footer { margin-top: 30px; font-size: 0.8rem; color: #666; }
    </style>
</head>
<body>

<div class="container">
    <h1>最新訪問地址導航</h1>
    
    <div id="links-container"></div>

    <div class="footer">
        建議收藏本頁面 (Ctrl+D) <br>
        如遇地址失效，請刷新本頁獲取最新鏈接
    </div>
</div>

<script>
    /**
     * 💡 以后要换域名，只需要修改这里！
     * 为防止被爬虫抓取，URL 建议使用 Base64 编码
     * 编码工具：https://tool.oschina.net/encrypt?type=3
     */
    const config = [
        { 
            name: "最新網址 (1)", 
            desc: "推薦使用 - 訪問最流暢", 
            url: "aHR0cHM6Ly9tMWZ1cGluZy5sb2wv" // https://m1fuping.lol
        },
        { 
            name: "最新網址 (2)", 
            desc: "備用地址 - 海外加速", 
            url: "aHR0cHM6Ly9yYXBpZHRhaS5jb20=" // https://rapidtai.com
        },
        { 
            name: "最新網址 (3)", 
            desc: "備用地址 - 備用節點", 
            url: "aHR0cHM6Ly90YWltYWRvdS5jb20=" // https://taimadou.com
        }
    ];

    const container = document.getElementById('links-container');

    config.forEach(item => {
        const card = document.createElement('a');
        card.className = 'card';
        // 解码跳转
        card.href = 'javascript:void(0);';
        card.onclick = () => {
            window.location.href = atob(item.url);
        };
        
        card.innerHTML = `
            <h2>${item.name}</h2>
            <p>${item.desc}</p>
        `;
        container.appendChild(card);
    });
</script>

</body>
</html>
