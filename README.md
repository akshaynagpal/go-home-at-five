# Go Home At Five
### List of most common small mistakes that take a lot of time to debug and prevents developers to go home at 5PM.

- Sending AJAX Post Request    
    `JSON.stringify()` if you are sending JSON.
- 0 means False when evaluated as a Boolean.
    ```
    if hashmap[key]:
        do something
    else:
        do something else
    ```
    Here, if the value is 0, the above if condition will return false, even when there is an element in the hashmap with the given `key`.

- Avoid using `:` character in `id` attribute of a HTML `div` element.    
    As a purely practical matter, you may want to avoid certain characters. Periods, colons and '#' have special meaning in CSS selectors, so you will have to escape those characters using a backslash in CSS or a double backslash in a selector string passed to jQuery. Think about how often you will have to escape a character in your stylesheets or code before you go crazy with periods and colons in ids.
    
    For example, the HTML declaration `<div id="first.name"></div>` is valid. You can select that element in CSS as `#first\.name` and in jQuery like so: `$('#first\\.name')`. But if you forget the backslash, `$('#first.name')`, you will have a perfectly valid selector looking for an element with id first and also having class name. This is a bug that is easy to overlook. You might be happier in the long run choosing the id first-name (a hyphen rather than a period), instead. [Source](https://stackoverflow.com/a/79022/3120481)

- Python - Using mutable default value (`list`, `dict` etc) for function arguments.   
    This can lead to trippy behavior explained at https://stackoverflow.com/questions/1132941/least-astonishment-and-the-mutable-default-argument which further directs to http://effbot.org/zone/default-values.htm . TLDR- functions are first class objects in python.

- Java - parseBoolean VS getBoolean [TODO]

