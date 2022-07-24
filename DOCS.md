just include/require the library, there are 3 options you could define :  
  
`DPXImageServer_Storage` : Path to save files and Keep Caches (insure that it is writable)  
  
`DPXImageServer_TTL` : Amount of time that a file cache is valid (In Seconds), Set it to 0 to disable caching (ofcourse if you lost your mind ! why would you disable cache ?)  
  
`DPXImageServer_PNGQuant` : Path of PNGQuant Binary, for PNG Compression we use libpngquant and has to be installed on the Server, Otherwise the uncompressed image would be returned  
  
  
There is only a function `DPXServeImage` with these parameters :  

`file_path` : path of the image file to be served (Required | String)  
  
`width` : Desired width of image (Optional | Integer)  
  
`height` : Desired height of image (Optional | Integer)    
  
`quality` : Desired quality of image, a Number between 10-100 (Optional | Integer)
  
`output_image` : Wether the image would be outputted or just return the string of the image  
  
`cache` : Wether to cache the image or not  
  
if Image file you have given is not found or an Invalid format, `DPXServerImage` would return false

also keep in mind that if you pass only one of width or height params, the other one will be calculated respectivly, maintaining aspect ratio

That's all I can tell right now, But I'll try to document it well later in a better way (also you are welcome to do it too)
