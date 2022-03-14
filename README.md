<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<meta name="viewport" content="initial-scale=1.0, user-scalable=no" />
	<style type="text/css">
	body, html,#containers {width: 100%;height: 100%;overflow: hidden;margin:0;font-family:"微软雅黑";}
	</style>
	<script src="https://api.map.baidu.com/api?v=2.0&&type=webgl&ak=fHecfmYdTGstiIIM3CAFDZ1iYUwgcqbc"></script>
	<title>My hometown</title>
</head>
<body>
	<div id="containers"></div>
    <script type="text/javascript">

	var map = new BMapGL.Map("containers");    // 创建Map实例
	var point = new BMapGL.Point(114.65, 33.62);
	var marker = new BMapGL.Marker(point);  // 创建标注
	map.centerAndZoom(new BMapGL.Point(114.65, 33.62), 11);  // 初始化地图,设置中心点坐标和地图级别
	map.enableScrollWheelZoom(true);     //开启鼠标滚轮缩放
	map.addOverlay(marker);              // 将标注添加到地图中
    var sContent =
"<center><h4 style='margin:0 0 5px 0;padding:0.2em 0'>周口</h4></center>" +
"<img style='float:right;margin:4px' id='imgDemo' src='https://cn.bing.com/images/search?view=detailV2&ccid=Lio8LZgT&id=DF464D69E0419237A3065B574E9B1A917F9B08DC&thid=OIP.Lio8LZgTt0GzWEyJcbbEQAHaDt&mediaurl=https%3a%2f%2ftse1-mm.cn.bing.net%2fth%2fid%2fR-C.2e2a3c2d9813b741b3584c8971b6c440%3frik%3d3Aibf5Eam05XWw%26riu%3dhttp%253a%252f%252fwww.tangyin.gov.cn%252fsitesources%252ftyweb%252fupload%252f202001%252f20200124181230736.jpg%26ehk%3d6yF%252fP4dUVzbukwrbJwqurlDBUmfuLGGbOlhlTINpj6Q%253d%26risl%3d%26pid%3dImgRaw%26r%3d0&exph=640&expw=1280&q=%e5%b2%b3%e9%a3%9e%e7%ba%aa%e5%bf%b5%e9%a6%86&simid=608031416474426673&FORM=IRPRST&ck=AE950224FB9300BD59DA3B1FAFD97227&selectedIndex=7&qft=+filterui%3aimagesize-custom_800_600&ajaxhist=0&ajaxserp=0' width='200' height='104' title='岳飞纪念馆'/>"  +
"<a style='color:#1C2B35;text-decoration:none;' href='https://baike.baidu.com/item/%E5%91%A8%E5%8F%A3/139270'>click it for more information</a>"
"</div>";

var infoWindow = new BMapGL.InfoWindow(sContent);     // marker添加点击事件
	marker.addEventListener('click', function () {
   		 this.openInfoWindow(infoWindow);
});

</script>
</body>
</html>
