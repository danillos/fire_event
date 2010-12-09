Simple Event Handler class in PHP, great for add plugins to your application.

## Example

    Event::fire('initialize');
    ...
    Event::add('initialize','show_hello');

    function show_hello() {
	      echo 'Hello World on initializer';
    }