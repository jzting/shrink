Shrink
======

Given a single HTML file as input, Shrink will insert your JavaScript and CSS inline. Shrink uses YUI and HTML Compressor to compress your JS and HTML.

Configuration
-------------
Update the following paths to their respective locations:

        YUI_COMPRESSOR_PATH = "/PATH/TO/yuicompressor-2.4.6.jar"
        HTML_COMPRESSOR_PATH = "/PATH/TO/htmlcompressor-1.5.2.jar"

Wrap any external CSS and JS with the following comment tags:

        <!-- BEGIN: Uncompressed CSS -->
        <link rel="stylesheet" href="css/main.css">
        <!-- END: Uncompressed CSS -->  
        
        <!-- BEGIN: Uncompressed JS -->  
        <script src="js/main.js"></script>
        <!-- END: Uncompressed JS -->

Optionally, symlink to your /usr/local/bin directory:
        
        ln -s /PATH/TO/SHRINK/shrink /usr/local/bin
    
Usage
-----
        ./shrink input_file.html output_file.html 
        
If no output file is given, it will write to compressed.html

