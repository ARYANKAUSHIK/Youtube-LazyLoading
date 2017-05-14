# Youtube-LazyLoading

Embedding a Youtube video has become a completely normal process for anyone involved with the web; copy, paste, done. However, pulling in an external resource like a Youtube video may slow down a web page’s load performance, especially if there are two or more videos embedded on the same page.

By embedding videos we request more than just a video file. A number of resources are fetched, including JavaScript files, a stylesheet, images, and advertisements.

##Script for lazy-load
``` javascript
  //fetching element
    var youtube = document.getElementById("youtube");
    //source for image provided by youtube..in this url add your video id here 'kF9NMCJFyHk'
    var source ="https://img.youtube.com/vi/kF9NMCJFyHk/sddefault.jpg";
    var image = new Image();
    image.src = source;
    
    image.addEventListener( "load", function() {
            youtube.appendChild(image);
            });
     //on  click load the vedio
    youtube.addEventListener( "click", function() {
        var iframe = document.createElement( "iframe" );
        iframe.setAttribute( "frameborder", "0" );
        iframe.setAttribute( "allowfullscreen", "" );
        iframe.setAttribute( "src", "https://www.youtube.com/embed/kF9NMCJFyHk?rel=0&autoplay=1");
            this.innerHTML = "";
            this.appendChild( iframe );
    } ); 
'''

This will reduce the page load time on-demand load the file.
