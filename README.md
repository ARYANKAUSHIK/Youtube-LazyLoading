# Youtube-LazyLoading

Embedding a Youtube video has become a completely normal process for anyone involved with the web; copy, paste, done. However, pulling in an external resource like a Youtube video may slow down a web page’s load performance, especially if there are two or more videos embedded on the same page.

By embedding videos we request more than just a video file. A number of resources are fetched, including JavaScript files, a stylesheet, images, and advertisements. And as you can from the screenshot below, two Youtube videos equates to 22 HTTP requests with a total of 624kb downloaded. These numbers will climb as we embed more videos on the page.