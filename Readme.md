PhoneGap ToastPlugin
==============

* Author: HondaDai
* License - The MIT License
* Test on PhoneGap 1.7.0 (cordova 1.7)


Install Step (On Eclipse)
--------------------------

1. Import File System to folder **src**, select **ToastPlugin.java**
2. Edit **res\xml\plugins.xml**, add `<plugin name="ToastPlugin" value="com.phonegap.plugin.ToastPlugin"/>` into `<plugins> </plugins>`
3. Import **ToastPlugin.js** into .html

API
-----

### Standard
	window.plugins.Toast.show( Message, Duration, SuccessCallback, FailureCallback);
	
### USE Toast.LENGTH_SHORT
	window.plugins.Toast.show( Message, **window.plugins.Toast.LENGTH_SHORT**, SuccessCallback, FailureCallback);
	or
	window.plugins.Toast.shortshow( Message, SuccessCallback, FailureCallback); 
	
### USE Toast.LENGTH_LONG
	window.plugins.Toast.show( Message, **window.plugins.Toast.LENGTH_SHORT**, SuccessCallback, FailureCallback);
	or
	window.plugins.Toast.longshow( Message, SuccessCallback, FailureCallback);
	
Example
--------

	document.addEventListener("deviceready", onDeviceReady, false);
	function onDeviceReady(){
		window.plugins.Toast.show("Text To Show" , 500);
		
		$('#showlong').click(function(){
			window.plugins.Toast.longshow("lazy use long");
		});
		$('#showshort').click(function(){
			window.plugins.Toast.shortshow("lazy use short");
		});
	};
