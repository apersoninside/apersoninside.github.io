# yeetus.github.io
<html>
<head>
<meta name="apple-mobile-web-app-capable" content="yes">
<meta id="title" name="apple-mobile-web-app-title" content="Proxy">

<link id="icon" rel="apple-touch-icon" href="round_cydia_icon_by_5284973_d4khkre_fullview_m8Z_icon.ico">
<link rel="icon" href="round_cydia_icon_by_5284973_d4khkre_fullview_m8Z_icon.ico">
<link rel="shortcut icon" href="round_cydia_icon_by_5284973_d4khkre_fullview_m8Z_icon.ico">
  
<title>Proxy</title>
</head>
<body>
<div id="bruv" width="100%" height="100%" style="position:fixed; top:0; left:0; bottom:0; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;">
<!-- pastes shit in here -->
<p>type a website</p>
<input type="text" id="textbox" value="https://">
<br>
<input type="text" id="urlicon" value="Ex. Https://krunker.io">
<input type="button" name="button" value="search" onclick="window.location.replace('https://yeetus.github.io/?url=' + encodeURIComponent(document.getElementById('textbox').value) + '&icon=' + encodeURIComponent(document.getElementById('urlicon').value));">
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
		document.getElementById("bruv").innerHTML = '<iframe src="' + decodeURIComponent(website) + '" width="100%" height="100%" style="position:fixed; top:0; left:0; bottom:50; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;">';
		document.getElementById("icon").href = decodeURIComponent(urlParams.get('icon'));
	}
</script>

</body>
</html>
