# Joeyyang111.github.io
<head>
    <meta charset="UTF-8">
    <title>my hometown</title>
    <style>
        #container
        {
            width: 800px;
            height: 400px;
        }
    </style>
    <script src="https://api.map.baidu.com/api?v=1.0&&type=webgl&ak=fHecfmYdTGstiIIM3CAFDZ1iYUwgcqbc"></script>
</head>
<body>
    <center>
    <h2>Welcome to my hometown——周口</h2>
    <div id="container"></div>
    <script>
        var map = new BMapGL.Map("container");
        var point = new BMapGL.Point(114.65, 33.62);
        map.centerAndZoom(point, 15);
    </script>
    <h2>Look,This is also the hometown of Lao Tzu</h2>
    <img src="laotzu.jpg" alt="图片替换文本" title="a wonderful image" width="800" height="400"/>
    <h2>If you want to learn more about my hometown,</h2>
    <a href="https://baike.baidu.com/item/%E5%91%A8%E5%8F%A3/139270">click here</a>
    </center>
</body>
