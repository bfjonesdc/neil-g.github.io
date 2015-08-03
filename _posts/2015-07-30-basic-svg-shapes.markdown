---
layout:     post
title:      "Basic SVG Shapes"
subtitle:   "Interactive look at Rectanlges, Ellipses, and Polylines"
date:       2015-07-21 12:00:00
author:     "Neil Gordon "
comments:   true
header-img: "img/post-bg-01.jpg"
---

<h1> Basic SVG Shapes </h1>

<p> The next basic svg shapes we'll go over int his article are: rectangles, circles (and ellipses), and polylines (polygons).  These shapes consist of 3 distinct parts: 1) spatial coordinates, 2) the border (or stroke), 3) the inside (or fill).  This is similar to the line in terms of having spatial coordinate and stroke parameters, but fill is new since these shapes have an "inside."</p> 



<!-- Name of Shape -->
<h1> Rectangle </h1>
<p> table here </p>


<!-- SVG element viewport -->
<div class="container">
  <div class="row">
    <div class="five columns">
      <h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;">
        <rect id="rect"
          x="10" y="10" width="50" height="50" 
          stroke="pink" stroke-width="3" stroke-opacity="1" stroke-dasharray="2,2" rx="5" ry="5"
          fill="blue" fill-opacity="0.8" />
        <!-- helpers -->
      </svg>
    </div>
    <div class="seven columns">
    	<h1> Code </h1>
<!-- HTML generated using hilite.me --><div style="background: #202020; overflow:auto;width:auto;border:solid gray;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #6ab825; font-weight: bold">&lt;svg&gt;</span>
  <span style="color: #6ab825; font-weight: bold">&lt;rect</span> <span style="color: #bbbbbb">id=</span><span style="color: #ed9d13">&quot;rect&quot;</span>
        <span style="color: #bbbbbb">x=</span><span style="color: #ed9d13">&quot;10&quot;</span> <span style="color: #bbbbbb">y=</span><span style="color: #ed9d13">&quot;10&quot;</span> <span style="color: #bbbbbb">width=</span><span style="color: #ed9d13">&quot;50&quot;</span> <span style="color: #bbbbbb">height=</span><span style="color: #ed9d13">&quot;50&quot;</span> 
        <span style="color: #bbbbbb">stroke=</span><span style="color: #ed9d13">&quot;pink&quot;</span> <span style="color: #bbbbbb">stroke-width=</span><span style="color: #ed9d13">&quot;3&quot;</span> <span style="color: #bbbbbb">stroke-opacity=</span><span style="color: #ed9d13">&quot;1&quot;</span> 
        <span style="color: #bbbbbb">stroke-dasharray=</span><span style="color: #ed9d13">&quot;2,2&quot;</span> <span style="color: #bbbbbb">rx=</span><span style="color: #ed9d13">&quot;5&quot;</span> <span style="color: #bbbbbb">ry=</span><span style="color: #ed9d13">&quot;5&quot;</span>
        <span style="color: #bbbbbb">fill=</span><span style="color: #ed9d13">&quot;blue&quot;</span> <span style="color: #bbbbbb">fill-opacity=</span><span style="color: #ed9d13">&quot;0.8&quot;</span> <span style="color: #6ab825; font-weight: bold">/&gt;</span>
<span style="color: #6ab825; font-weight: bold">&lt;/svg&gt;</span>
</pre></div>


      </div>
    </div>
  </div>
</div>

<!-- Input fields that toggle svg parameters -->
<div class="container">
  <div class="row">
    <h1> Toggle </h1>
  </div><!--row-->
  <div class="row">
    <div class="twelve columns">

      <label for="xInput"> x </label>
      <input class="u-full-width" type="number" id="xInput" />

      <label for="yInput"> y </label>
      <input class="u-full-width" type="number" id="yInput" />

      <label for="width">width</label>
      <input id="widthInput" type="number" class="u-full-width" />

      <label for="height">height</label>
      <input id="heightInput" type="number" class="u-full-width"/>

      <label for=""></label>
      <input id="strokeColorInput" type="text" class="u-full-width"/>

      <label for=""></label>
      <input id="strokeWidthInput" type="number" class="u-full-width"/>

      <label for=""></label>
      <input id="strokeOpacityInput" type="number" class="u-full-width"/>

      <label for=""></label>
      <input id="strokeDashInput" type="text" class="u-full-width"/>

      <label for=""></label>
      <input id="rxInput" type="number" class="u-full-width"/>

      <label for=""></label>
      <input id="ryInput" type="number" class="u-full-width"/>

      <label for=""></label>
      <input id="fillInput" type="text" class="u-full-width"/>

      <label for=""></label>
      <input id="fillOpacityInput" type="number" class="u-full-width"/>


    </div><!--twelve columns--> 
  </div><!--row-->
</div>



<h1> Circle </h1>
<p></p>

<h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;">
        <circle cx="20" cy="20" r="20" 
        stroke="purple" stroke-width="2" stroke-opacity="1" stroke-dasharray="3,3"
        fill="blue" fill-opacity="1"  />
        <!-- helpers -->
      </svg>



<h1> Ellipse </h1>
<p>Ellipses are similar to circles, except the radius in the x and y directions are separate values, allowing a shape to be wider than it is tall or vise versa.  A circle is an ellipse where there is one radius value for both directions.<p>
<h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;">
        <ellipse cx="20" cy="20" rx="20" ry="40" 
        stroke="purple" stroke-width="2" stroke-opacity="1" stroke-dasharray="3,3"
        fill="blue" fill-opacity="1"  />
        <!-- helpers -->
      </svg>



<h1> Polyline </h1>
<p>A polyline is a series of connecting lines that are drawn by between a series of points.  In other words, you specify a series of points, and lines are drawn from point to point in the order they are listed</p>
<h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;">
        <polyline points="10,10  20,20  20,50"
        stroke="purple" stroke-width="2" stroke-opacity="1" stroke-dasharray="3,3"
        fill="blue" fill-opacity="1"  />
        <!-- helpers -->
      </svg>


<h1> Polygon </h1>
<p>A polygon is the same as a polyline, except that it automatically closes the shape for you.  In other words, a line is automatically added connecting the last point to the first point.  In contrast, with a polyline, you would have to add this closing line manually by having the first point and last point be equal</p>
<h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;">
        <polygon points="10,10  20,20  20,50"
        stroke="purple" stroke-width="2" stroke-opacity="1" stroke-dasharray="3,3"
        fill="blue" fill-opacity="1"  />
        <!-- helpers -->
      </svg>



<script>

var rect = document.getElementById('rect')

// convenient setting functions
function setX(x) {
	rect.x.baseVal.val = x;
  rect.x.baseVal.value = x;
}

function setY(y) {
	rect.y.baseVal.val = y;
  rect.y.baseVal.value = y;
}

function setWidth(width) {
	rect.width.baseVal.val = width;
  rect.width.baseVal.value = width;
}

function setHeight(height) {
  rect.height.baseVal.val = height;
  rect.height.baseVal.value = height;
}

function setStrokeColor(color) {
  rect.height.baseVal.val = height;
  rect.height.baseVal.value = height;
}

function setStrokeWidth(width) {
  rect.attributes['stroke-width'].value = width;
  document.getElementById('strokeWidthCode').innerHTML = "&quot;" + width + "&quot;";
}

function setStrokeColor(color) {
  rect.attributes['stroke'].value = color;
  document.getElementById('strokeColorCode').innerHTML = "&quot;" + color + "&quot;";
}

function setStrokeOpacity(opacity) {
  rect.attributes['stroke-opacity'].value = opacity;
  document.getElementById('strokeOpacityCode').innerHTML = "&quot;" + opacity + "&quot;";
}

function setStrokeDash(dash) {
  rect.attributes['stroke-dasharray'].value = dash;
  document.getElementById('strokeDashCode').innerHTML = "&quot;" + dash + "&quot;";
}


function setRx(rx) {
  rect.rx.baseVal.val = rx;
  rect.rx.baseVal.value = rx;
}

function setRy(rx) {
  rect.ry.baseVal.val = ry;
  rect.ry.baseVal.value = ry;
}

// event listeners
document.getElementById('xInput').addEventListener('input', function(e){
	setX(e.target.value);
});

document.getElementById('yInput').addEventListener('input', function(e){
	setY(e.target.value);
});

document.getElementById('widthInput').addEventListener('input', function(e){
  setWidth(e.target.value);
});

document.getElementById('heightInput').addEventListener('input', function(e){
  setHeight(e.target.value);
});


document.getElementById('strokeColorInput').addEventListener('input', function(e){
  setStrokeColor(e.target.value);
});

document.getElementById('strokeWidthInput').addEventListener('input', function(e){
  setStrokeWidth(e.target.value);
});

document.getElementById('strokeOpacityInput').addEventListener('input', function(e){
  setStrokeOpacity(e.target.value);
});

document.getElementById('strokeDashInput').addEventListener('input', function(e){
  setStrokeDash(e.target.value);
});

document.getElementById('rxInput').addEventListener('input', function(e){
  setRx(e.target.value);
});

document.getElementById('ryInput').addEventListener('input', function(e){
  setRy(e.target.value);
});

document.getElementById('fillInput').addEventListener('input', function(e){
  setFill(e.target.value);
});

document.getElementById('fillOpacityInput').addEventListener('input', function(e){
  setfillOpacity(e.target.value);
});


</script>