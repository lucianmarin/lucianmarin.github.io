---
layout:     default
date:       2014-04-15 00:30
title:      "Animated 3D Logo in CSS"
category:   meaningful-labor
slug:       animated-logo-css
syntax:     true
---

I wanted to create a special logo for [Sublevel](http://sublevel.net/), a new product from me. I ended up with [an orbital solution](http://cssdeck.com/labs/single-element-orbitals) that was actually a hack on display refresh rate. Basically the refresh rate of a computer monitor is 60 Hz, but the circle rotated at an higher rate. It created the ilusion that there were more than one circle rotating.

Then I found that you can create very smooth 3D animated logos with CSS, if you carefully tweak *transform* and *animation* properties. In the case below I used to rotate a circle at 180deg on all XYZ axis, equally delay the animation of each circle and position them absolutely on top of each one. The result is pretty spectaluar if you ask a designer that loves static logos.

<div class="frame">
    <div class="orbital">
        <div class="one"></div>
        <div class="two"></div>
        <div class="three"></div>
        <div class="four"></div>
    </div>
</div>

#### CSS code

    @keyframes outer {
        to { transform: rotateX(180deg) rotateY(180deg) rotateZ(180deg); }
        }
    .orbital .one   { animation: outer 8s 0s infinite; }
    .orbital .two   { animation: outer 8s 2s infinite; }
    .orbital .three { animation: outer 8s 4s infinite; }
    .orbital .four  { animation: outer 8s 6s infinite; }

#### HTML code

    <div class="orbital">
        <div class="one"></div>
        <div class="two"></div>
        <div class="three"></div>
        <div class="four"></div>
    </div>

<style type="text/css">
@-webkit-keyframes outer {
    to {
        -webkit-transform: rotateX(180deg) rotateY(180deg) rotateZ(180deg);
        }
    }
@keyframes outer {
    to {
        transform: rotateX(180deg) rotateY(180deg) rotateZ(180deg);
        }
    }
.orbital {
    width: 50px;
    height: 50px;
    position: relative;
    margin: 0 auto;
    }
.orbital > div {
    width: 48px;
    height: 48px;
    position: absolute;
    display: block;
    border: 1px black solid;
    border-radius: 25px;
    }
.orbital .one {
    -webkit-animation: outer 8s 0s infinite;
    animation: outer 8s 0s infinite;
    }
.orbital .two {
    -webkit-animation: outer 8s 2s infinite;
    animation: outer 8s 2s infinite;
    }
.orbital .three {
    -webkit-animation: outer 8s 4s infinite;
    animation: outer 8s 4s infinite;
    }
.orbital .four {
    -webkit-animation: outer 8s 6s infinite;
    animation: outer 8s 6s infinite;
    }
</style>
