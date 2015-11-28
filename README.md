# BDTD3 
```html
<pre>

<!DOCTYPE html>
<html lang="fr">
<head>
	<title>Météo</title>
	<meta charset="utf-8">	
	<meta name="viewport" content="width=device-width, user-scalable=no">
	<meta name="viewport" content="width=500, initial-scale=1">
	<meta name="HandheldFriendly" content="true"/>  
	<link rel="stylesheet" type="text/css" href="css/style.css">
<script type="text/javascript" src="http://code.jquery.com/jquery-latest.min.js"></script>
	<!--[if lt IE 9]>
		<script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
	<![endif]-->
</head>
<body>

<div id="bloc_page">

	<header>	
		<div id="person">	
			<h1>Site Météo</h1>	
			<p>
				Nice<br />				
				France<br />				
			</p>
		</div>
		<div id="logo"><img src="img/logo.png" alt="LP DAM" title="LP DAM" /></div>
	</header>

	<section>
		<h2>Choisir Localisation</h2>
		<FORM id="Formulaire">
			Ville : <br> 
			<input type="text" id="idVille"> <br> 
			
			<input id="idMeteo"  type="button" value="Météo" onClick="chercheMeteo($('#idVille').val())"><br/>
			<script>
		var $ville=document.getElementById("idVille");
		function chercheMeteo(ville)
		{
			//alert("debut fonction");
			console.log("coucou");
			var $url="http://api.openweathermap.org/data/2.5/weather?q="+$('#idVille').val()+"&mode=html&appid=2de143494c0b295cca9337e1e96b00e0";
			var $type="GET";
			var $dataType="json";
	$('aside').append('<iframe src="'+$url+'" id="idaffich"></iframe>');
		}
		</script>
		</FORM>
		
	</section>

	<aside>
		<h2>Météo</h2>
	</aside>
	
	<footer>
		<h3>Footer</h3>
	</footer>
</div>
</body>
</html>
</pre>
```
