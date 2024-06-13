# JavaScript

## Printing Values

### Print Dynamic Copyright Year Range

Used to dynamically print the copyright year range as the starting year to current year _or_ as only the current year if it is the same as the starting year.

On page load, once all the JS has loaded, `getCopyrightYears()` is called with the starting year passed as a parameter. The contents of the markup (`<span id="copyrightYears">2023</span>`) are then replaced with the starting year to current year or just the current year, if it's the same as the starting year. The current year appears hard-coded in the markup body in case the JS doesn't load or run properly.

In `js/main.js`:

```javascript
function getCopyrightYears(copyrightStartYear) {
    const currentYear = new Date().getFullYear();
    let copyrightYears = '';

    if (currentYear > copyrightStartYear) {
        copyrightYears = copyrightStartYear + '-' + currentYear;
    } // end if test
    else {
        copyrightYears = copyrightStartYear;
    } // end else test

    return copyrightYears;
} // end getCopyrightYears function

$(document).ready(function() {
    const copyrightStartYear = 2023;
    $('#copyrightYears').text(getCopyrightYears(copyrightStartYear));
});
```

In `whatever.html`:

```html
  ...
  <p>Copyright © Some Company <span id="copyrightYears">2023</span></p>
  <! -- jQuery includes go here -->
  <script src="/js/main.js"></script>
  ...
```

When the current year matches the starting year (e.g., 2023), the output generated is: `Copyright © Some Company 2023`

When the current year (e.g., 2025) _does not_ match the starting year (e.g., 2023), the output generated is: `Copyright © Some Company 2023-2025`

## Data Handling

### Deep Copy Array

See [Guitar Diagrams JS issue #42](https://github.com/KCarlile/guitar-diagrams-js/issues/42) for reference.

The `reverse()` method on an array mutates the original array, so assigning an array to another variable and then calling `reverse()` on the new reference _also_ changes the original array. For example:

```javascript
let arr1 = [1, 2, 3];
let arr2 = arr1.reverse();

// now BOTH arrays are [3, 2, 1]
```

As a workaround, deep copy the array like this:

```javascript
let arr1 = [1, 2, 3];
let arr2 = [...arr1].reverse();

// now arr1 is [1, 2, 3] and arr2 is [3, 2, 1]
```
