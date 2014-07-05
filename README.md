#BeefUp

A jQuery Accordion Plugin

Demo: http://beefup.schaschaweb.de/

## Usage

1. Include jQuery
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>

2. Include plugin
    <script src="jquery.beefup.min.js"></script>

3. Add markup
    <article class="beefup">
        <h2 class="beefup-head">Headline</h2>
        <div class="beefup-body">My fancy collapsible content.</div>
    </article>

4. Call the plugin
    <script>
        $(function() {
            $('.beefup').beefup();
        });
    </script>

## Configuration

    trigger			: '.beefup-head'        // String: Name of the trigger element
    content			: '.beefup-body'        // String: Name of the collapsible content
    openClass		: 'open'				// String: Name of the class which shows if a accordion is triggered or not
    openSingle		: false                 // Boolean: Open just one accordion at once
    animation		: 'slide'               // String: Set animation type, "slide" or "fade"
    showSpeed		: 200                   // Integer: Set the speed of the show animation
    hideSpeed		: 200                   // Integer: Set the speed of the hide animation
    scroll			: fale              	// Boolean: Scroll to accordion
    scrollSpeed     : 400					// Integer: Set the speed of the scroll feature
    scrollOffset	: 0                     // Integer: Additional offset to accordion position
    onInit			: function(){}          // Callback: Fires after the initially setup
    onOpen			: function(){}			// Callback: Fires after accordion open the content
    onClose			: function(){}			// Callback: Fires after accordion close the content

## Advanced

1. Open accordion
    $('.beefup').beefup().open($('#beefupID'));

2. Close accordion
    $('.beefup').beefup().close($('#beefupID'));

3. Scroll to accordion
    $('.beefup').beefup().scroll($('#beefupID'));

4. Callback method
    $('.beefup').beefup({
        onInit: function ($this) {
            // Do something after initially setup
        },
        onOpen: function ($this) {
            // Do something after accordion open the content
        },
        onClose: function ($this) {
            // Do something after accordion close the content
        }
    });

## Bugs?

Please let me know: https://github.com/Schascha/BeefUp/issues