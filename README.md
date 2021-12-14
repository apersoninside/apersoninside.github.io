# apersoninside.github.io
  
<!doctype html>
<html>

<body>
<div id="bruv" width="100%" height="100%" style="position:fixed; top:0; left:0; bottom:0; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;">
<!-- pastes shit in here -->
<p>type a website</p>
<input type="text" id="textbox" value="https://">
<br>
<input type="text" id="urlicon" value="https://">
<input type="button" name="button" value="search" onclick="window.location.replace('https://apersoninside.github.io/?url=' + encodeURIComponent(document.getElementById('textbox').value) + '&icon=' + encodeURIComponent(document.getElementById('urlicon').value));">
</div>

<script>
	function wait(ms) {
		var d = new Date();
		var d2 = null;
		do { d2 = new Date(); }
		while(d2-d < ms);
	}

	const queryString = window.location.search;
	const urlParams = new URLSearchParams(queryString);
	if (urlParams.has('url')) {
		const website = urlParams.get('url');
		const ico = "http://www.google.com/s2/favicons?domain=" + website;
		wait(1000);
		document.getElementById("bruv").innerHTML = '<iframe src="' + decodeURIComponent(website) + '" width="100%" height="100%" style="position:fixed; top:0; left:0; bottom:0; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;">';
		document.getElementById("icon").href = decodeURIComponent(urlParams.get('icon'));
	}
</script>

</body>
  
  
