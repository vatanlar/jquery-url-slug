
<div align="">
  <h3 align="">Javascript URL Slug Generate</h3>
  <p align="">
    Create Clean Slug from String.
  </p>
</div>


```javascript

// Convert "Hello World! How Are You?" => "/hello-world-how-are-you/"

function permalink(val) {

    var accepted_letters = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "r", "s", "t", "u", "v", "y", "x", "w", "z", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "-"];

    val = val.replace(/ /g, "-");
    val = val.replace(/İ/g, "i");
    val = val.replace(/ı/g, "i");
    val = val.replace(/ğ/g, "g");
    val = val.replace(/Ğ/g, "g");
    val = val.replace(/Ç/g, "c");
    val = val.replace(/ç/g, "c");
    val = val.replace(/ü/g, "u");
    val = val.replace(/Ü/g, "u");
    val = val.replace(/Ö/g, "o");
    val = val.replace(/ö/g, "o");
    val = val.replace(/Ş/g, "s");
    val = val.replace(/ş/g, "s");

    val = val.replace(/[^a-z0-9\s]/gi, '-').replace(/[_\s]/g, '-')

    for (let i = 0; i < val.length; i++) {
        val = val.replace(/--/g, "-");
    }

    if (val.substr(-1) == "-") {
        val = val.slice(0, -1);
    }

    if (val.charAt(0) == "-") {
        val = val.slice(1);
    }
    val = val.toLowerCase();

    return val;
}
```
