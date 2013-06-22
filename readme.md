# Adrian's Css Hack

First up search for Chrome Canary and install it...

or go here https://www.google.com/intl/en/chrome/browser/canary.html

In your address bar type:

chrome://flags

find and enable
 - Enable experimental WebKit features.
 - Experimental Extension APIs

restart your browser (or computer if you're on the windows)

## Scoped Variables:

    html {
        -webkit-var-brandcolor: orange;
    }

    section {
     -webkit-var-brandcolor: red;
     }

     h1 { color: -webkit-var(brandcolor)  }



## Supports:

Apply a better style if it's supported:

(thumbs-up isn't actually a thing - if it was and the browser supported it, we'd get it.)

    li {list-style-type: circle  }

    @supports (list-style-type: thumbs-up) {
        li {list-style-type: thumbs-up  }
    }


# Anchor based styles
targets... so - if you're on http://my-cool-site.com/index#MY-TARGET

Your element with id MY-TARGET will have this style applied:

  :target {
      background:blue;
  }



## Targeting stuff by what it isn't

ol li:not(:last-of-type) {
    color: green;
}

nav a:not(.selected) {
color: gray
}


## Styling the placeholder...

input:placeholder-shown {
    font-size:100px
}



## Target by validity

input:invalid {
    border:5px red solid;
}


<label for='number'>a number</label> <input id='number' required pattern='\d*' />


## Flex!

This doesnt work in chrome yet - try firefox nightly: (also, it's insanely important. I haven

    <ul>
      <li>some</li>
      <li>elements</li>
      <li>a load of theadsfsf sdf dsf sdfg tterg the text</li>
      <li>yeah</li>
      <li>Wooooooo!</li>
    </ul>


    .theflexboxyeah ul {
        display:flex;
    }

    .theflexboxyeah li{
        flex:auto;
        border: 1px solid red;
        list-style-type:none;
    }

or

    .theflexboxyeah li{
        flex:1;
        border: 1px solid red;
        list-style-type:none;
    }


    .theflexboxyeah li:nth-child(2) {
        flex:2;
    }