# Adding-a-Flash-Video-to-Your-Pages

This example uses the OS FLV player to display a video called puppy.flv, which has already been convered into FLV format.You have already seen how to use SWFObject to embed a 
basic animation in a page, but sometimes Flash movies need information in order for them to work. In this example, the video player needs to know the path to the video it has to play, so SWFObject uses JavaScript variables to pass this information to the Flash movie. These are provided in the two lines of code that start with var.This particular player is not expecting any information in the flashvars variable, so that is left empty.The path to the movie is supplied in the variable called params.var params = {movie:"../videos/puppy.flv"};The line after the variables is the one that tells the script to replace the HTML element with the video player. It is very similar to the one you saw in the earlier example that introduced SWFObject.

<!DOCTYPE html>
<html>
  <head>
    <title>Adding a Flash Video</title>
    <script type="text/javascript" 
     src="http://ajax.googleapis.com/ajax/libs/
     swfobject/2.2/swfobject.js"></script>
     <script type="text/javascript">
     var flashvars = {};
     var params = {movie:"../video/puppy.flv"};
     swfobject.embedSWF("flash/splayer.swf", 
     "snow", "400", "320", "8.0.0", 
     flashvars, params);</script>
  </head>
  <body>
    <div id="snow"><p>A video of a puppy playing in  the snow</p></div>
  </body>
</html>
