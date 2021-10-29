<!DOCTYPE html>
<html>
<head>
	<title>test</title>
	<style type="text/css">
		*{
			-webkit-user-select: none;
		}
	</style>
</head>
<body>
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
