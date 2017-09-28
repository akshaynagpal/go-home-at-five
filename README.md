# Go Home At Five
### List of most common small mistakes that take a lot of time to debug and prevents developers to go home at 5PM.

- Sending AJAX Post Request    
    `JSON.stringify()` if you are sending JSON.
- 0 means False
    ```
    if hashmap[key]:
        do something
    else:
        do something else
    ```
    Here, if the value is 0, the above if condition will return false, even when there is an element in the hashmap with the given `key`.

-
