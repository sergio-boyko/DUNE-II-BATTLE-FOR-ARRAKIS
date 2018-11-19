# DUNE-II-BATTLE-FOR-ARRAKIS

Файлы игры и эмулятор. Две версии игры в папке files.
```
\files
	dune-the-battle-for-arrakis-eng.gen - англ версия игры
	dune-the-battle-for-arrakis-rus.gen - рус версия игры
	Nesbox.swf - эмулятор (только для flash)
```
js.html - js версия эмуляторв
```
<!-- JS version -->
	<link rel="stylesheet" href="//mem.neptunjs.xyz/neptun/css/neptun.css" type="text/css">
	<div id="emu" style="width: 300;"></div>
	<script> 
			var NepDefCon = '1';			 
			var NepPlayer = "#emu";			 
			var NepEmu = "sega";			 
			var NepZoom = "enable";			 
			var NepMaxWidth = "100%";			 
			var NepAutoStart = true;			 
			var NepLang = "rus";			 
			var gameUrl = "flash/dune-the-battle-for-arrakis-rus.gen";			 
			var SaveTitle = "dune-the-battle-for-arrakis";
	</script>

	<script src="https://mem.neptunjs.com/njs/njsLoader.js" type="text/javascript"></script>
	<!--/ JS version -->
```
flash.html - flash версия эмулятора
```
<!-- Flash version -->
<object type="application/x-shockwave-flash" data="flash/Nesbox.swf" width="640" height="480" id="emulator" style="visibility: visible; width: 640px; height: 448px;"><param name="allowscriptaccess" value="sameDomain"><param name="allowFullScreen" value="true"><param name="allowFullScreenInteractive" value="true"><param name="flashvars" value="dune-the-battle-for-arrakis.gen"></object>
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js"></script>
<script src="//ajax.googleapis.com/ajax/libs/swfobject/2.2/swfobject.js"></script>
<script type="text/javascript">	
	var resizeOwnEmulator = function(width, height) {		
		var emulator = $('#emulator');
		emulator.css('width', width);
		emulator.css('height', height);		
	}
	$(function() {
		function embed() {
			var emulator = $('#emulator');
			if (emulator) {
				var flashvars = {
					system : 'sega',
					url : 'flash/dune-the-battle-for-arrakis-rus.gen',
				};
				var params = {};
				var attributes = {};
				params.allowscriptaccess = 'sameDomain';
				params.allowFullScreen = 'true';
				params.allowFullScreenInteractive = 'true';
				swfobject.embedSWF('flash/Nesbox.swf', 'emulator', '640', '480', '11.2.0', 'flash/expressInstall.swf', flashvars, params, attributes);
            }
        }
		embed();
	});
</script>
<!--/ Flash version -->
```