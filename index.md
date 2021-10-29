<!DOCTYPE html>
<html>
<head><meta name="viewport" content="minimal-ui, width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">

	<meta name="mobile-web-app-capable" content="yes">
	<meta name="apple-mobile-web-app-capable" content="yes">
	<link rel="manifest" href="/manifest.json">
	<title>test</title>
	<style type="text/css">
		*{
			-webkit-user-select: none;
		}
	</style>
</head>
<body>
<script> function requestFullScreen() {

  var el = document.body;

  // Supports most browsers and their versions.
  var requestMethod = el.requestFullScreen || el.webkitRequestFullScreen 
  || el.mozRequestFullScreen || el.msRequestFullScreen;

  if (requestMethod) {

    // Native full screen.
    requestMethod.call(el);

  } else if (typeof window.ActiveXObject !== "undefined") {

    // Older IE.
    var wscript = new ActiveXObject("WScript.Shell");

    if (wscript !== null) {
      wscript.SendKeys("{F11}");
    }
  }
}


</script>
<a href="#" onClick="requestFullScreen();"> click </a>
<h1>Hey</h1>
<p>Lorem ipsum dolor sit amet consectetur si la retu rectusic nupoti tryi kule jun hexen meti.</p>
<input type="submit" name="submit" id="submit">
<script type="text/javascript">
	
	function getFullscreenElement(){
		return document.fulllscreenElement
		|| document.webkitFullscreenElement
		|| document.mozFullscreenElement
		|| document.msFullscreenElement;
	}

	function toggleFullscreen(){
		if (getFullscreenElement()) {
			document.exitFullscreen();
		} else {
			document.documentElement.requestFullscreen().catch(console.log);
		}
	}
	const x = document.getElementById("submit");
	x.addEventListener("click", () => {toggleFullscreen()});

</script>

</body>
</html>
