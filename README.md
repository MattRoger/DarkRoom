# DarkRoom :film_strip:
Dark Room service webpage

[See the site](https://mattroger.github.io/DarkRoom/)

## Why This Project?
I had an idea for a landing page to turn a negative image into a positive for a friends dark room business. :bulb:

## Build Status
All That needs to be done is personalize the content and add verification to the contact form. :heavy_check_mark:

## Tech/framework used
 * Javascript
 * jQuery
 * Bootstrap
 * Adobe Photoshop
 
## Features
An intro where and image fades from a negative to a positive using the .fadeOut fucntion and CSS Positioning 	:fire:

## Take A Tour

#### The Intro
![intro](https://github.com/MattRoger/screenshots/blob/master/darkroom/DarkRoom.gif?raw=true)
#### The Body of the site
Where the user can learn about the printer, see pricing, and contact the printer.
![tour](https://github.com/MattRoger/screenshots/blob/master/darkroom/tour.gif?raw=true)

## How I made it! :man_mechanic:

### Step 1
* Inverted my image in photoshop and then made an adjustment to the middle tones. I chose this way becuase it had more controll that the css filter:invert(100%). However if you wish to replicate this effect, then give it a try!

### Step 2 The HTML

I used Bootstrap as the frame work for this project.

```HTML
 <header>
        <div class="headerWrapper">
<!--Start with the negative image and black text -->
            <div class="head neg">
                <div class="headTextWrapper">
                    <p class="h1">LeRoy's DarkRoom Printing</p>
                    <div class="mainNav">
                        <a href="#about">About</a>
                        <a href="#pricing">Pricing</a>
                        <a href="#contact">Contact</a>
                    </div>
                </div>
                <img src="assets/img/neg.jpg" class="img-fluid" alt="Responsive image">
            </div>
         
<!--Positive image with white text  -->
            <div class="head pos">
                <div class="headTextWrapper">
                    <p class="h1">LeRoy's DarkRoom Printing</p>
                    <div class="mainNav">
                        <a href="#about">About</a>
                        <a href="#pricing">Pricing</a>
                        <a href="#contact">Contact</a>
                    </div>
                </div>
                <img src="assets/img/pos.jpg" class="img-fluid" alt="Responsive image">
            </div>
        </div>
    </header>
```
### The CSS

```CSS
.headWrapper{
    position: relative;
}
.head{
    position: relative;
    height: 100vh;
    overflow: hidden;
    font-family: 'Overpass Mono', monospace;
}

.head .headTextWrapper{
    text-align: center;
    position: absolute;
    width:100%;
    top:50vh;
}
.h1{
    font-size: 3em;
    
}
.head a{
    font-size: 2.5em;
    padding:1em;
}
.pos .h1{
    color:white;
}
.pos a{
    color:white;
}
.neg{
    z-index: 100;
    position: absolute;
    top:0
}
.neg a{
    color: black;
}

```

### The JavaScript

```javascript
$(document).ready(function () {
    fade()
})

function fade() {
    console.log("working")
    $(".neg").fadeOut(7000)
}
```

## Installation
* :trident: Fork it
* :sheep: Clone it


## Credits / Contact information
* @MattRoger 
  * :man_office_worker: https://mattroger.github.io/
  * :e-mail: mattroger.webdev@gmail.com
  * :man_office_worker: www.linkedin.com/in/matt-roger/

©All Content Matt Roger
