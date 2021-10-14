# apersoninside.github.io



const queryString = window.location.search;
const urlParams = new URLSearchParams(queryString);
if (urlParams.has('url')) {
	const website = urlParams.get('url');
	const ico = "http://www.google.com/s2/favicons?domain=" + website;
	wait(1000);
	document.getElementById("bruv").innerHTML = '<iframe src="' + decodeURIComponent(website) + '" width="100%" height="100%" style="position:fixed; top:0; left:0; bottom:50; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:999999;">';
	document.getElementById("icon").href = decodeURIComponent(urlParams.get('icon'));
}
