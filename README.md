<!DOCTYPE html>
<html>
<head>
	<title>Binary Clock</title>
	<link rel="shortcut icon" href="logo.png">
	<meta name="description" content="Binary Clock API, just one step to inplement it in your webpage">
	<meta name="author" content="Bichiko(harry) Kodua">
	<meta name="keywords" content="clock, binary, API, Plugin">
	<meta property="og:title" content="Binary-Clock">
	<meta property="og:description" content="Binary Clock API, just one step to inplement it in your webpage">
	<meta property="og:image" content="https://bichiko.github.io/binary-clock/logo.png">
	<meta http-equiv="content-type" content="text/html;charset=UTF-8">
</head>
<link href="https://fonts.googleapis.com/css?family=Bree+Serif" rel="stylesheet">
 <style type="text/css">
::-webkit-scrollbar {
width: 6px;
/* for vertical scrollbars */
height: 6px;
/* for horizontal scrollbars */
}

::-webkit-scrollbar-track {
	background: rgba(0, 0, 0, 0.1);
}

::-webkit-scrollbar-thumb {
	background: rgba(255, 100, 0, 0.5);
}
 h1{
	font-family: 'Nosifer', cursive;
 }
 h3,h6,p{
 	font-family: 'Bree Serif', serif;
 }
 	h1,h3,h6{
 		margin: auto;
 		text-align: center;
 		color: rgba(255,100,0,0.5);
 	}
 	.container{
 		width: 1000px;
 		height: auto;
 		border: solid 1px rgba(255,100,0,0.5);
 		margin: 30px auto;
 		padding: 20px 20px;
 		border-radius: 5px;
 		box-shadow: 1px 1px 10px rgba(255,100,0,0.5);
 		background-color: rgba(255,100,0,0.02);
 	}
 	hr{
 		border-color:rgba(255,100,0,0.1);
 		width: 70%;
 		margin: 30px auto;
 	}
 	p{
 		padding: 10px;
 		color: rgba(255,100,0,0.7);
 	}
 	.innerDiv{
 		width: 70%;
 		height: auto;
 		border-radius: 5px;
 		border:solid 1px rgba(255,100,0,0.5);
 		margin: 40px auto;
 		text-align: center;
 		padding: 30px;
 		background-color: rgba(255,100,0,0.04);
 		position: relative;
 		overflow: hidden;
 	}
 	code{
 		/*background-color: white;*/
 		/*border: solid 1px red;*/
 		/*margin: 20px auto;*/
 		/*padding: 20px;*/
 		text-align: left;
 		width: 70%;
 	}

 	em{
		display: inline-block;
		padding: 0 5px 0 3px;
		border-radius: 3px;
		color: rgba(255,0,0,0.7);
		background-color: rgba(0,0,0,0.1);
		font-family: 'Roboto', sans-serif;
		font-weight: unset;
	}
	pre{
		text-align: left;
		width: 50%;
		margin: auto;
		background-color: white;
		border-radius: 5px;
		color: rgba(255,100,0,0.8);
 		border: solid 1px red;
 		margin: 20px auto;
 		padding: 10px 40px;
	}
	.followme,.generate{
		width: 150px;
		font-size: 20px;
		height: 50px;
		background-color: rgba(255,100,0,0.5);
		border:solid 1px rgba(255,100,0,0.4);
		border-radius: 5px;
		color: rgba(255,100,0,0.9);
		cursor: pointer;
		transition: 0.5s all;
	}
	.followme:hover, .generate:hover{
		background-color: rgba(255,100,0,0.6);
		border:solid 1px rgba(255,100,0,0.5);
	}
	label{
		color: rgba(255,100,0,0.7);
		font-size: 16px;
	}
	span{
		font-size: 12px;
	}
	input[type=number]{
		width: 40px;
		border: solid 1px rgba(255,100,0,0.5);
		padding-left: 5px;
		border-radius: 1px;
	}
	input[type=color]{
		width: 20px;
		border: solid 1px rgba(255,100,0,0.5);
		border-radius: 1px;
		background-color: rgba(255,100,0,0.1);
		cursor: pointer;
	}
	.generated{
		resize: none;
		overflow: hidden;
		height: 140px;
		width: 80%;
		font-size: 10px;
		display: none;
		margin: auto;
		padding-left: 10px;
		padding-top: 6px;
		color: rgba(255,100,0,0.9);
	}
	.apiurl{
		resize: none;
		overflow: hidden;
		height: 40px;
		width: 80%;
		margin: auto;
		font-size: 10px;
	}
	.hidden{
		display: none;
	}
	::-moz-selection { /* Code for Firefox */
    color: white;
    background: rgba(255,0,0,0.6);
}

::selection {
    color: white; 
    background: rgba(255,0,0,0.6);
}
 </style>
<link href="https://fonts.googleapis.com/css?family=Nosifer" rel="stylesheet">
<script type="text/javascript" src="js.js"></script>

<body>
<div class="container">
	<h1><em>Binary</em> Clock API</h1>
	<hr>
<div class="nohidden">
	
	<div class="innerDiv">
		<h3>Do you want Binary Clock in your web page?</h3>
		<br>
		<script type='text/javascript' class='binaryClock'> 
			var tempcl =  new binaryClock({	    
				width: 300, 	    
				height: 50,	    
				labels: true,	    
				labelcolor: 'rgba(255,100,0,0.4)',	    
				emptybitcolor: 'rgba(255,100,0,0.6)',	    
				filledbitcolor: 'rgba(255,100,0,0.9)'
			});
		</script>
		<pre>
		<code>
if(yes){
	new Element()
	.create('button')
	.html('Follow me');
}
		</code>
		</pre>

		<button class="followme">Follow me</button>
	</div>
	<script type="text/javascript">
	var initClock = null
	var defaultColors = {
		label: '#1a3c6c',
		ebitColor: '#6d6ecc',
		fBitColor: '#ff0000'
	}


		window.onload = function(){
			document.getElementsByName('labelcolor')[0].value = defaultColors.label
			document.getElementsByName('filledbitcolor')[0].value = defaultColors.fBitColor
			document.getElementsByName('emptybitcolor')[0].value = defaultColors.ebitColor

			document.querySelector('.followme').onclick=function(){
				document.querySelector('.hidden').style.display='block'
				document.querySelector('.nohidden').style.display='none'
				tempcl.srcRemove()
				initClock = new binaryClock({
					width: 200,
					height: 30,
					labels: false,
					labelcolor: defaultColors.label,
					emptybitcolor: defaultColors.ebitColor,
					filledbitcolor: defaultColors.fBitColor
				})
			}
		}
	</script>
		
	<br>
	<br>
	<br>
	<hr>
</div>
	<div class="hidden">
	<h3>You can fully customize Binary Clock</h3>
	<div class="innerDiv">
		<h3>Please enter data</h3>
		<hr>
		<label for="labels">Show Labels?:</label>
		<span><i>show</i></span><input type="checkbox"  name="label" value="true">
		<br>
		<br>
		<label for="width">Width:</label>
		<input type="number" name="width" value="300"><span> px; </span>
		<label for="height">Height:</label>
		<input type="number" name="height" value="50"><span> px</span>
		<br>
		<br>
		<label for="bgcolor">Label color:</label>
		<input type="color" name="labelcolor" value="#ffff44"><span> ; </span>
		<label for="filledbitcolor">Filled bit color:</label><span> ; </span>
		<input type="color" name="filledbitcolor" value="#cf4455">
		<label for="emptybitcolor">Empty bit color:</label><span> ; </span>
		<input type="color" name="emptybitcolor" value="#cc33ff">
		<hr>
		<h3>Live Preview</h3>
		<br>
		<script type="text/javascript" class='binaryClock'>



			

			var elements = [
				{
					object: document.querySelector('input[name=width'),
					value: 300,
					name: 'width'
				},
				{
					object: find('input[name=height').element,
					value: 50,
					name: 'height'
				},
				{
					object: find('input[name=label').element,
					value: false,
					name: 'label'
				},
				{
					object: find('input[name=labelcolor').element,
					value: defaultColors.label,
					name: 'labelcolor'
				},
				{
					object: find('input[name=emptybitcolor').element,
					value: defaultColors.ebitColor,
					name: 'emptybitcolor'
				},
				{
					object: find('input[name=filledbitcolor').element,
					value: defaultColors.fBitColor,
					name: 'filledbitcolor'
				}
			]

			elements.forEach(function(element, index){
				element.object.onchange = function(){
					element.value = this.value
					initClock.remove()
					initClock = new binaryClock({
						width: elements[0].value,
						height: elements[1].value,
						labels: (this.name == 'label'?(this.checked?'true':'false'):elements[2].value),
						labelcolor: elements[3].value,
						emptybitcolor: elements[4].value,
						filledbitcolor: elements[5].value
					})
					showCode();
				}
			})



		</script>
		<div class="innerDiv">
		<p>Place this code wherever you want the plugin to appear on your page.</p>
			<textarea onclick="this.select()" class="generated" spellcheck="false"></textarea>
		<hr>
		</div>

	</div>
</div>



<script type="text/javascript">
		function showCode(){
				document.querySelector('.generated').style.display="block"
					document.querySelector('.generated').innerHTML = ""+
						"&lt;script type='text/javascript' src='https://bichiko.github.io/binary-clock/js.js'>&lt;/script>\n"+
						"&lt;script type='text/javascript' class='binaryClock'>\n"+
						"new binaryClock({\n"+
						"  width: "+elements[0].value+",\n"+
						"  height: "+elements[1].value+",\n"+
						"  labels: "+(elements[2].value==1?'true':'false') +",\n"+
						"  labelcolor: '"+elements[3].value+"',\n"+
						"  emptybitcolor: '"+elements[4].value+"',\n"+
						"  filledbitcolor: '" + elements[5].value+"'"+
						"\n});\n"+
						"&lt;/script>"
		}	
		showCode()
</script>
</div>

</body>
</html>
