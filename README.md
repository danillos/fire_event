Simple Event Handler class in PHP, great for add plugins to your application.

## Example

    Event::fire('initialize');
		...
		$body = 'Danillo';
		Event::fire('finish',&body);
		echo $body;
    ...
    Event::add('initialize','init');
		Event::add('finish','show_hello');
		
		// simple
    function init() {
	      echo 'Starting...';
    }
		
		// callback with reference args
    function show_hello(&$body) {
	      $body = 'Hello World '.$body;
    }