# Audio-Player
Audio Player is a simple but powerful extremely customizable responsive audio player that can play local, self-hosted or streaming mp3 files, ShoutCast &amp; IceCast radio servers or stations HLS / m3u8 / HTTP Live Streaming, SoundCloud, Google Drive, Amazon S3, Dropbox and more.

A) Important notes make sure you read this!
Please note that the Easy Audio Player installation and configuration is not complicated but because it has a lot of customizable settings it might seem complicated, please go through the entire documentation before trying to install it into your own page. Basically what it must be done is to copy some html code from the examples we provided and paste it into your own html page and of course add your own audio file.

The server is character case sensitive so make sure that the Easy Audio Player settings are identical to those from the provided examples.

When testing local on IE7/IE8 it will not work because the flash (.swf) file is trying to comunicate with the browser and this is not allowed, of course it will work fine when tested online.

B) Preparing the audio files.
This audio player requires only .mp3, there is no need to suply an .ogg or other type of audio source.

C) Preparing SHOUTCAST.
In order to stream shoutcast instead on adding the source mp3 file path add the shoutcast server address and at the end of it ;.mp3 , like this : http://95.141.24.224:80/;.mp3. Adding the ;.mp3 at the end of the address will force the server to serve the mp3 stream instead of the http web page. Please note that this player has support only for mp3 stream and it will not work correctly with other formats like .acc or .ogg. The good news is that the player will play the stream on all browser no matter which operating system is used, this applies to both mobile and desktop.

D) How to install Easy Audio Player into your html page.
This is a small tutorial about how to install the Easy Audio Player into your page. Easy Audio Player can be e embedded into a html page inside a div of your choosing, the Easy Audio Player will adapt its width based on the maxWidth property specified in the constructor, the height is set based on the skin height, if the page is resized and the parent div width is smaller then the maxWidth property the Easy Audio Player will adapt its size accordingly.

In the download files inside the start folder there are html files starting with the label "skin", each of this examples have exactly the same structure with different constructor settings you can use one of them to copy and paste the needed html code based on skin that you need, I will use the skin-minimal-white.html as an example for this tutorial.

The skin is created using javascript and .png images, if you want a custom skin please contact us. If you want to create a skin of your own modify the ones we already provided.

Copy and paste the content folder and the java folder into the same folder with your .html file, inside the content folder there are other folders which are self explanatory. Keep only the skin folders that you need to save space on the server.
Open skin-minimal-white.html with a text editor.
The javascript file must be imported, in the head section of your html file add the code from the below image.

  <style type="text/javascript" src="content/global.css"></style>
  <script type="text/javascript" src="java/FWDEAP.js"></script>

You need a div into which the Easy Audio Player will be added as a child, so create a div and set an id for it, the id is important because it is passed in the Easy Audio Player constructor, make sure it is unique. The Easy Audio Player is responsive as follows, the width will adapt based on the maxWidth property specified in the constructor, the height is set based on the skin height, if the page is resized and the parent div width is smaller then the maxWidth property the Easy Audio Player will adapt its size accordingly.
  
  <div id="myDiv"></div>

Next step is to set the audio path, to do this in the contructor set the sourcePath property, the path can be relative or absolute and it must point to a mp3 file.

Next step is to initialize the Easy Audio Player with javascript, in the head section of your html page add the code from the below image. Please note that all parameters are described in the constructor parameters section

<script type="text/javascript">
    FWDEAPUtils.onReady(function(){
        new FWDEAP({        
            //main settings
            instanceName:"player1",
            parentId:"myDiv",
            mainFolderPath:"content", 
            skinPath:"minimal_skin_dark",
            sourcePath:"content/mp3/1.mp3",
            useOnlyAPI:"no",
            rightClickContextMenu:"developer",
            addKeyboardSupport:"yes",
            initializeOnlyWhenVisible:"no",
            autoPlay:"no",
            loop:"yes",
            soundCloudAPIKey:"",
            useHEXColorsForSkin:"no",
            normalHEXButtonsColor:"#FF0000",
            normalHEXButtonsColor2:"#00FF00",
            maxWidth:750,
            volume:.8,
            //controller settings
            animateOnIntro:"yes",
            useVectorIcons:"no",
            showOnlyPlayButton:"no",
            showBackgroundBar:"yes", 
            showMainScrubber:"yes",
            showTime:"yes",
            showVolumeScrubber:"yes",
            showVolumeButton:"yes",
            showToolTips:"yes",
            positionPlayButton:"first",
            repeatBackground:"no",
            controllerHeight:47,
            startSpaceBetweenButtons:16,
            spaceBetweenButtons:10,
            volumeScrubberWidth:80,
            scrubbersOffsetWidth:2,
            scrubbersOffestTotalWidth:3,
            timeOffsetLeftWidth:5,
            timeOffsetRightWidth:2,
            timeOffsetTop:0,
            timeOffestTotalWidth:4,
            timeColor:"#888888",
            toolTipBackgroundColor:"#FFFFFF",
            toolTipTextColor:"#000000",
            //visualizer
            useVisualizer:'yes',
            visualizerRandomPreset:"yes",
            visualizerPreset:"wave1",
            visualizerColor:["#AAAAAA", "#999999", "#888888", "#777777", "#666666"],
            visualizerCapColor: "#FFFFFF"
        });
    });
</script>

This is how the player is installed in a HTML page, please read the Constructor parameters section to understand the Easy Audio Player properties

E) Constructor parameters.
Please open any of the .html files provided with a text editor as reference.

These parameters represents the possible setting for the Easy Audio Player they are all visible in the below image and described below.
<script type="text/javascript">
    FWDEAPUtils.onReady(function(){
        new FWDEAP({        
            //main settings
            instanceName:"player1",
            parentId:"myDiv",
            mainFolderPath:"content", 
            skinPath:"minimal_skin_dark",
            sourcePath:"content/mp3/1.mp3",
            useOnlyAPI:"no",
            rightClickContextMenu:"developer",
            addKeyboardSupport:"yes",
            initializeOnlyWhenVisible:"no",
            autoPlay:"no",
            loop:"yes",
            soundCloudAPIKey:"",
            useHEXColorsForSkin:"no",
            normalHEXButtonsColor:"#FF0000",
            normalHEXButtonsColor2:"#00FF00",
            maxWidth:750,
            volume:.8,
            //controller settings
            animateOnIntro:"yes",
            useVectorIcons:"no",
            showOnlyPlayButton:"no",
            showBackgroundBar:"yes", 
            showMainScrubber:"yes",
            showTime:"yes",
            showVolumeScrubber:"yes",
            showVolumeButton:"yes",
            showToolTips:"yes",
            positionPlayButton:"first",
            repeatBackground:"no",
            controllerHeight:47,
            startSpaceBetweenButtons:16,
            spaceBetweenButtons:10,
            volumeScrubberWidth:80,
            scrubbersOffsetWidth:2,
            scrubbersOffestTotalWidth:3,
            timeOffsetLeftWidth:5,
            timeOffsetRightWidth:2,
            timeOffsetTop:0,
            timeOffestTotalWidth:4,
            timeColor:"#888888",
            toolTipBackgroundColor:"#FFFFFF",
            toolTipTextColor:"#000000",
            //visualizer
            useVisualizer:'yes',
            visualizerRandomPreset:"yes",
            visualizerPreset:"wave1",
            visualizerColor:["#AAAAAA", "#999999", "#888888", "#777777", "#666666"],
            visualizerCapColor: "#FFFFFF"
        });
    });
</script>

//----main----//
instanceName:"player1" - The player instance name, trough this instance the API is called for example if the instance name is "player1" and if you want to call play of this instance it is called like this player1.play();. Please note that the instance name must be unique for each instance.
parentId:"myDiv" - The id of the div into which the Easy Audio Player is added, this id must be unique for each instance.
mainFolderPath:"content" - The path of the folder that contains the skins and flash file.
sourcePath:"audio.mp3" - the .mp3 source path.
useOnlyAPI:"no" - this can be yes or no, if is set to yes the Easy Audio Player buttons and skin will not be loaded and you will have an invisible instance of the player, this is useful for custom audio players.
rightClickContextMenu:"default" - this can be developer, default or disabled. We would appreciate it if you can leave this feature set to developer.
autoPlay:"no" - this can be yes or no.
loop:"no" - this can be yes or no.
soundCloudAPIKey:"api1key" - the SoundCloud API key, more keys can be added separated by comma (key1, key2, key3 etc...) this way if one key fails the other ones will be used until one is valid and works, this also applies if the quota has been used for the 24 hours time. EAP has 8 keys included so it should work fine but if you do have your own keys please used them.
maxWidth:450 - a number that represents the player maximum width in px, think of this property as it would be the max-width css property.
volume:.5 - A number from 0 to 1 that represents the volume level.
backgroundColor:"transparent" - the entire background color, usualy this is transparent but you can set it to any color you like.
animateOnIntro:"yes" - this can be yes or no, once the Easy Audio Player is ready the buttons will appear in place with a short animation, this behavior can be disabled by setting this property to no.
showOnlyPlayButton:"yes" - this can be yes or no.
showBackgroundBar:"yes" - this can be yes or no.
showMainScrubber:"yes" - this can be yes or no.
showFacebookButton:"yes" - this can be yes or no.
showVolumeScrubber:"yes" - this can be yes or no.
showVolumeButton:"yes" - this can be yes or no.
showToolTips:"yes" - this can be yes or no.
positionPlayButton:"yes" - this can be first or last.
showTime:"yes" - this can be yes or no.
repeatBackground:"yes" - this can be yes or no.
progressScrubberMinWidth:300 - a number that represents the scrubber minimum width in pixels, if the scrubber width is less then this number buttons will be removed from the player.
volumeScrubberWidth:80 - a number that represents the volume srubber width in pixels.
startSpaceBetweenButtons:10 - a number that represents the start space between buttons, ilustrated below with the red arrows.
spaceBetweenButtons:10 - a number that represents the space between buttons, ilustrated below with the red arrows.
scrubbersOffsetWidth:10 - a number that represents the total amount in pixels removed from the scrubber bars progress line when they are at the end (change number to understand it better, useful based on the skin type).
scrubbersOffestTotalWidth:10 - a number that represents the total amount in pixels removed from the entire scrubber bars when they are the last element/button (change number to understand it better, useful based on the skin type).
timeOffsetLeftWidth:10 - a negative or positive number that represents the offset left of the time, this will push the time left or right (change number to understand it better, useful based on the skin type).
timeOffsetRightWidth:10 - a negative or positive number that represents the offset right of the time, this will push the time left or right (change number to understand it better, useful based on the skin type).
timeOffsetTop:10 - a negative or positive number that represents the offset top of the time, this will push the time up or down (change number to understand it better, useful based on the skin type).
timeOffestTotalWidth:10 - a number that represents the total amount in pixels removed from the entire time when it is the last element/button (change number to understand it better, useful based on the skin type).
timeColor:#FFFFFF - time font color.
//-- visualizer --//
useVisualizer:"yes" - this can be yes or no. Set it to yes to enable the audio Visualizer. Please note this will not work on locahost and it will only work with audio mp3 files.
visualizerRandomPreset:"no" - this can be yes or no. Set it to yes to set a random visualizer preset each time the page loads.
visualizerPreset:"wave1" - this can be wave1, wave2, bars1 or bars2.
visualizerColor:["#AAAAAA", "#999999", "#888888", "#777777", "#666666"] - the visualizer color, it contains five colors that can be set as you want, do not remove or add any extra colors!
visualizerCapColor:"#FFFFFF" - the visualizer cap color if the preset is bars1.

F) Encrypt source path
To encrypt the source path I have created a tool that will encrypt the source path at this link, enter the source path (this applies all formats) in the input field then click on the Encrypt media button, once this is done copy the encrypted track path and paste it as the track source parameter.this is showed below. In this example content/mp3/01.mp3 is encrypted to encrypt:Y29udGVudC9tcDMvMDEubXAz .

G) API
Inside the donwload files there is HTML file called API-example.html, in this file I have added all events and methods for reference, open the page source to see them.
