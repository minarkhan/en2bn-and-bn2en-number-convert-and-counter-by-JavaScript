# English to bangla and bangla to english number convert and thats number counter by JavaScript

##Quickstart

### 1. Clone Repository
```sh
$ https://github.com/minarkhan/en2bn-and-bn2en-number-convert-and-counter-by-JavaScript
```

### 2. Run
```sh
$ Index.html run inside browser
```

### 2. Code.
```sh
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h1 class="bnCount">৪৯৪৯২২৪৯২</h1>
    <h1 class="enCount">789654223632</h1>
    <h1 class="bnCount">৪৯৪৯২২৪৯২</h1>
    <h1 class="enCount">789654223632</h1>
    <h1 class="bnCount">৪৯৪৯২২৪৯২</h1>
    <h1 class="enCount">789654223632</h1>
    <h1 class="bnCount">৪৯৪৯২২৪৯২</h1>
    <h1 class="enCount">789654223632</h1>

    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.5/jquery.min.js"></script>
    <script>
        var en2bnnumbers = {
            0: '০',
            1: '১',
            2: '২',
            3: '৩',
            4: '৪',
            5: '৫',
            6: '৬',
            7: '৭',
            8: '৮',
            9: '৯'
        };
        var bn2ennumbers = {
            '০': 0,
            '১': 1,
            '২': 2,
            '৩': 3,
            '৪': 4,
            '৫': 5,
            '৬': 6,
            '৭': 7,
            '৮': 8,
            '৯': 9
        };

        function replaceEn2BnNumbers(input) {
            var output = [];
            for (var i = 0; i < input.length; ++i) {
                if (en2bnnumbers.hasOwnProperty(input[i])) {
                    output.push(en2bnnumbers[input[i]]);
                } else {
                    output.push(input[i]);
                }
            }
            return output.join('');
        }

        function replaceBn2EnNumbers(input) {
            var output = [];
            for (var i = 0; i < input.length; ++i) {
                if (bn2ennumbers.hasOwnProperty(input[i])) {
                    output.push(bn2ennumbers[input[i]]);
                } else {
                    output.push(input[i]);
                }
            }
            return output.join('');
        }
        $('.bnCount').each(function() {
            var $this = $(this);
            var nubmer = replaceBn2EnNumbers($this.text());
            jQuery({
                Counter: 0
            }).animate({
                Counter: nubmer
            }, {
                duration: 2000,
                easing: 'swing',
                step: function() {
                    var nn = Math.ceil(this.Counter).toString();
                    $this.text(replaceEn2BnNumbers(nn));
                }
            });
        });
        $('.enCount').each(function() {
            var $this = $(this);
            var nubmer = $this.text();
            jQuery({
                Counter: 0
            }).animate({
                Counter: nubmer
            }, {
                duration: 2000,
                easing: 'swing',
                step: function() {
                    var nn = Math.ceil(this.Counter).toString();
                    $this.text(nn);
                }
            });
        });
    </script>
</body>

</html>
```
### Happy Coding...!
```sh
$ Happy Coding...!
```
