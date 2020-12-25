# CSS ACCORDION
###### Pure CSS accordion
###### [DEMO](https://chiranjit2020.github.io/css-accordion/index.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#e91e63">
    <link rel="icon" href="favicon.png" type="image/png" sizes="16x16">
    <title>Merry Christmas</title>
    <!-- Main Font -->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Carter+One&display=swap" rel="stylesheet">
    <!-- Title Font-->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Parisienne&display=swap" rel="stylesheet">
    <!-- Custom CSS Link -->
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="overlay">
        <div class="container">
            <h1>Merry Christmas</h1>
            <div class="accord">
                <div class="accord_item">
                    <input type="radio" id="heading1" name="title" checked>
                    <label class="accord_header" for="heading1">
                        <h5>What is Christmas?</h5>
                    </label>
                    <div class="accord_body">
                        <p>Christmas was traditionally a Christian festival celebrating the birth of Jesus, but in the early 20th century, it also became a secular family holiday, observed by Christians and non-Christians alike. The secular holiday is often devoid of Christian elements, with the mythical figure Santa Claus playing the pivotal role.</p>
                    </div>
                </div> <!-- .accord-item -->

                <div class="accord_item">
                    <input type="radio" id="heading2" name="title">
                    <label class="accord_header" for="heading2">
                        <h5>When is Christmas celebrated?</h5>
                    </label>
                    <div class="accord_body">
                        <p>Christmas is celebrated by many Christians on December 25 in the Gregorian calendar. For Eastern Orthodox churches that continue to use the Julian calendar for liturgical observances, this date corresponds to January 7 on the Gregorian calendar. Gifts are exchanged on Christmas Eve in most European countries and on Christmas morning in North America.</p>
                    </div>
                </div> <!-- .accord-item -->

                <div class="accord_item">
                    <input type="radio" id="heading3" name="title">
                    <label class="accord_header" for="heading3">
                        <h5>How is Christmas celebrated?</h5>
                    </label>
                    <div class="accord_body">
                        <p>Christians and non-Christians participate in some of the most popular Christmas traditions, many of which have no origins in Christianity. These customs include decorating evergreen trees—or, in India, mango or bamboo trees; feasting (picnics and fireworks are popular in warm climates); and exchanging gifts on Christmas Eve or Christmas morning.</p>
                    </div>
                </div> <!-- .accord-item -->

                <div class="accord_item">
                    <input type="radio" id="heading4" name="title">
                    <label class="accord_header" for="heading4">
                        <h5>Does Christmas have pagan roots?</h5>
                    </label>
                    <div class="accord_body">
                        <p>In ancient Rome, December 25 was a celebration of the Unconquered Sun, marking the return of longer days. It followed Saturnalia, a festival where people feasted and exchanged gifts. The church in Rome began celebrating Christmas on December 25 in the 4th century during the reign of Constantine, the first Christian emperor, possibly to weaken pagan traditions.</p>
                    </div>
                </div> <!-- .accord-item -->

                <div class="accord_item">
                    <input type="radio" id="heading5" name="title">
                    <label class="accord_header" for="heading5">
                        <h5>Did Christmas start in Germany?</h5>
                    </label>
                    <div class="accord_body">
                        <p>Christmas did not start in Germany, but many of the holiday’s traditions began there, including decorating trees. The celebration of Christmas started in Rome about 336, but it did not become a major Christian festival until the 9th century.</p>
                    </div>
                </div> <!-- .accord-item -->
            </div>
        </div>
    </div>
</body>
</html>
```
```css
*,
*::after,
*::before {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

html {
    font-size: 62.5%;
}

body {
    padding: 0;
    margin: 0;
    background-color: #ebebeb;
    font-family: 'Carter One', cursive;
}

.overlay {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container {
    width: 70rem;
    margin: 0 3rem;
}

.accord .accord_item {
    margin-bottom: 1rem;
}

.accord .accord_item .accord_header {
    display: block;
    padding: 2rem 1rem;
    background: rgb(233, 30, 99);
    background: linear-gradient(135deg, rgba(233, 30, 99, 1) 26%, rgba(0, 112, 255, 1) 100%);
    background-size: 150% 150%;
    border-radius: .5rem;
    color: #000;
    position: relative;
    cursor: pointer;
    -webkit-animation: animate 3s ease infinite;
    -moz-animation: animate 3s ease infinite;
    -o-animation: animate 3s ease infinite;
    animation: animate 3s ease infinite;
}

.accord .accord_item input {
    display: none;
}

.accord .accord_item .accord_header h5 {
    font-family: 'Carter One', cursive;
    font-size: 1.8rem;
    color: #fff;
    line-height: 1.3;
    letter-spacing: .1rem;
    transition: .5s;
    cursor: pointer;
    text-shadow: 0 .1rem black;
}

.accord .accord_item .accord_header::after {
    content: '\002B';
    position: absolute;
    right: 3%;
    top: 50%;
    transform: translateY(-50%);
    font-size: 2.5rem;
    color: #fff;
}

.accord .accord_item .accord_body {
    padding: 2rem;
    background-color: #fff;
    display: none;
    box-shadow: 0 .5rem 1.5rem 0 rgba(0, 0, 0, 0.25);
    border-radius: 0 0 .5rem .5rem;
}

.accord .accord_item input:checked ~ .accord_header::after {
    content: '\2212';
}

.accord .accord_item input:checked ~ .accord_body {
    display: block;
}

.accord .accord_item input:checked ~ .accord_header {
    border-radius: .5rem .5rem 0 0;
}

.accord .accord_item .accord_body p {
    font-size: 1.6rem;
    color: #242424;
    line-height: 1.5;
    padding: 0;
    margin: 0;
}

.container h1 {
    font-family: 'Parisienne', cursive;
    font-size: 8rem;
    color: #000;
    font-weight: 400;
    line-height: .8;
    text-align: center;
    padding: 0;
    margin: 0 0 5rem 0;
}

@-webkit-keyframes animate {
    0% {
        background-position: 0% 50%
    }

    50% {
        background-position: 100% 51%
    }

    100% {
        background-position: 0% 50%
    }
}

@-moz-keyframes animate {
    0% {
        background-position: 0% 50%
    }

    50% {
        background-position: 100% 51%
    }

    100% {
        background-position: 0% 50%
    }
}

@-o-keyframes animate {
    0% {
        background-position: 0% 50%
    }

    50% {
        background-position: 100% 51%
    }

    100% {
        background-position: 0% 50%
    }
}

@keyframes animate {
    0% {
        background-position: 0% 50%
    }

    50% {
        background-position: 100% 51%
    }

    100% {
        background-position: 0% 50%
    }
}

@media screen and (max-width: 480px) {
    html {
        font-size: 50%;
    }

    .container h1 {
        font-family: 'Parisienne', cursive;
        font-size: 7rem;
        color: #000;
        font-weight: 400;
        line-height: .8;
        text-align: center;
        padding: 0;
        margin: 0 0 3rem 0;
    }
}
```
