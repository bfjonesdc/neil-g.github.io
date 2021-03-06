---
layout:     post
title:      "Introduction to SVG"
subtitle:   "Interactive look at lines and the viewport"
date:       2015-07-21 12:00:00
author:     "Neil Gordon "
comments:   true
header-img: "img/post-bg-01.jpg"
---
<div class="container">
  <div class="row">
   		
	   	<!-- Name of Shape -->
	  	<h1> What is SVG </h1>
		


			<p> SVG stands for Scalable Vector Graphics.  It is used to define vector-based graphics for the web using XML format.  Some advantages of using svg is that  the quality of SVG graphics do not deteriorate as images are scaled up and down, and images can be transformed and animated. These graphics can be created and manipulated using any text editor, although there are many programs out there such as Inkscape and Adobe Illustrator that allow you to work with svg outside of text format. There are more robust introductions to svg there that I'll link to below, but for the purposes of this discussion, we'll be looking at simple svg shapes implanted directly onto the webpage as xml between svg tags. For understanding the elementary svg shapes this should be enough to get started.</p>

			<h1> The SVG Line </h1>
			<p> Our first shape is the line. Although lines are simple, and kind of boring, they serve as an important building block for almost every other shape. Below is an interactive drawing of a line.  On the right is the svg code, and on the left is the svg drawing that the code generates.  The things to pay attention to here are the parameters for the line.  The parameters can be thought of in two distinct parts: parameters that determine the spatial characteristics of the line, and parameters that determine the style of the line (its stroke).  Spatial is kind of like the where, and stroke is kind of like the how.</p>
	</div>
	<div class="row">
		<div class="columns six">
			<table>
	      <thead>
	         <tr>
	            <th>Spatial Parameter</th>
	            <th>description</th>
	         </tr>
	      </thead>
	      <tbody>
	         <tr>
	            <td>x1</td>
	            <td>x-coordinate of the beginning of the line</td>
	         </tr>
	         <tr>
	            <td>y1</td>
	            <td>y-coordinate of the beginning of the line</td>
	         </tr>
	         <tr>
	            <td>x2</td>
	            <td>x-coordinate of the end of the line</td>
	         </tr>
	         <tr>
	            <td>y2</td>
	            <td>y-coordinate of the end of the line</td>
	         </tr>
	      </tbody>
	   	</table>
	  </div>
		<div class="columns six">
   		<table class="table">
	      <thead>
	         <tr>
	            <th>Stroke Style Parameters</th>
	            <th>description</th>
	         </tr>
	      </thead>
	      <tbody>
	         <tr>
	            <td>stroke-width</td>
	            <td>width of the line</td>
	         </tr>
	         <tr>
	            <td>stroke-opacity</td>
	            <td>number btwn 0 and 1 representing line opacity (see-through-ness); </td>
	         </tr>
	         <tr>
	            <td>stroke</td>
	            <td>line color; can be a collor name like "yellow" or a color code like "#ffffff" or "#fff"</td>
	         </tr>
	          <tr>
	            <td>stroke-dasharray</td>
	            <td>dash pattern of line; two or more comma separated integers </td>
	         </tr>
	      </tbody>
	    </table>
		</div>
	</div>
</div>

<div class="container">
	<div class="row">
		<div class="columns five">
<!-- SVG element viewport -->

      <h1> SVG drawing </h1>
      <svg style="height: auto; width: 100%; border:1px solid blue;" xmlns="http://www.w3.org/2000/svg">
        <line id="line"
          x1="10"  
          y1="50" 
          x2="180"   
          y2="50" 
          stroke="purple"
          stroke-opacity = "1"
          stroke-width = "2"
          stroke-linecap = "square"
          stroke-dasharray = "5,5,6" />
        <text id="startCoordinates" x="10" y="30">10, 50</text>
        <text id="endCoordinates" x="180" y="50">180, 50</text>
      </svg>
    </div>

    <div class="columns seven">

<!-- SVG code representation -->

			<h1> Code </h1>
			<!-- HTML generated using hilite.me -->
			
  <pre style="margin: 0; line-height: 125%"><span style="color: #8B008B; font-weight: bold">&lt;svg</span> <span style="color: #658b00">xmlns=</span><span style="color: #CD5555">&quot;http://www.w3.org/2000/svg&quot;</span>
    <span style="color: #658b00">xmlns:xlink=</span><span style="color: #CD5555">&quot;http://www.w3.org/1999/xlink&quot;</span><span style="color: #8B008B; font-weight: bold">&gt;</span>

    <span style="color: #8B008B; font-weight: bold">&lt;line</span> 
      <span style="color: #658b00">x1=</span><span style="color: #CD5555" id="startXCode">&quot;65&quot;</span> <span style="color: #658b00">y1=</span><span style="color: #CD5555" id="startYCode">&quot;100&quot;</span> 
      <span style="color: #658b00">x2=</span><span style="color: #CD5555" id="endXCode">&quot;0&quot;</span> <span style="color: #658b00">y2=</span><span style="color: #CD5555" id="endYCode">&quot;100&quot;</span> 
      <span style="color: #658b00">stroke-width=</span><span style="color: #CD5555" id="strokeWidthCode">&quot;1&quot;</span> <span style="color: #658b00">stroke=</span><span style="color: #CD5555" id="strokeColorCode">&quot;red&quot;</span> 
      <span style="color: #658b00">stroke-opacity=</span><span style="color: #CD5555" id="strokeOpacityCode">&quot;1&quot;</span> <span style="color: #658b00">stroke-dasharray=</span><span style="color: #CD5555" id="strokeDashCode">&quot;5,5&quot;</span><span style="color: #8B008B; font-weight: bold">/&gt;</span>
      
<span style="color: #8B008B; font-weight: bold">&lt;/svg&gt;</span>
</pre>
			
		</div>
	</div>
</div>






    


<!-- Input fields that toggle svg parameters -->
<!-- Input fields that toggle svg parameters -->
<div class="container">
  <div class="row">
  	<div class="twelve columns">
    	<h1> Toggle </h1>
  	</div><!--twelve columns-->
  </div><!--row-->
  <div class="row">
    <div class="two columns">
      <label for="startX"> x1 </label>
      <input class="u-full-width" type="number" id="startX" />
      <label for="endX"> x2 </label>
      <input class="u-full-width" type="number" id="endX" />
    </div><!--two columns-->
    <div class="two columns">
      <label for="startY"> y1 </label>
      <input class="u-full-width" type="number" id="startY"/>
      <label for="endY"> y2 </label>
      <input class="u-full-width" type="number" id="endY" />
    </div><!--two columns-->
    <div class="three columns">
      <label for="strokeWidth"> stroke width </label>
      <input class="u-full-width" type="number" id="strokeWidth" min="0" />
      <label for="strokeOpacity"> stroke opacity </label>
      <input class="u-full-width" type="number" id="strokeOpacity" min="0" max="1" step=".01" />
    </div><!--two columns-->
    <div class="three columns">
      <label for="strokeColor"> stroke color </label>
      <input class="u-full-width" type="text" id="strokeColor" />
      <label for="strokeDash"> dash pattern </label>
      <input class="u-full-width" type="text" id="strokeDash" />
    </div><!--three columns-->
  </div><!--row-->
</div><!--container-->

<div class="container">
  <div class="row">
<h1>The Viewport, Viewbox, and Coordinate System</h1>

<p> Every SVG drawing is done inside of a viewport.  The dimension of the viewport can be determined by the width and height parameters in the opening svg tag.  In the previous line example, the viewport has a blue border around it so you can see the drawing area more clearly.    

Inside this Viewport, spatial orientation is determined by a coordinate system.  The standard (Cartesian) coordinate system has its origin (0,0) in the bottom left corner, and x increases as you move to the right, and y increases as you move up.  The svg coordinate system is similar but with a reversed y-coordinate orientation.  In other words, the origin is in the top left (not bottom left), and y increases as you go down (not up).  You can see this as you change the y1 and y2 coordinates of the line in the previous example.

Inside the Viewport, is also a Viewbox.  The Viewbox is essentially an area inside the Viewport that you are focusing on.  You can think of it like zooming in on any rectangular area of the larger Viewport.  The area of the Viewbox is also determined in the starting svg tag. </p>


<div>
      <h1> Viewbox View </h1>
      <svg height="300" width="500" style="border:1px solid blue;" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" id ="svgViewBox">
        <line id="line"
          x1="10"  
          y1="50" 
          x2="180"   
          y2="50" 
          stroke="purple"
          stroke-opacity = "1"
          stroke-width = "2"
          stroke-linecap = "square"
          stroke-dasharray = "5,5" />
        <circle cx="10" cy="10" r="2" fill="blue" id="dot1" />
        <text x="10" y="10" id="dot1Text" >(10, 10)</text>
      </svg>
</div>


<div>
      <h1> Viewport View with Viewbox </h1>
      <svg height="300" width="500" style="border:1px solid blue;" xmlns="http://www.w3.org/2000/svg" id ="svgViewPort">
      	<rect x="0" y="0" stroke="blue" fill-opacity="0" height="30" width="30" id="rectViewBox" />
        <line id="line"
          x1="10"  
          y1="50" 
          x2="180"   
          y2="50" 
          stroke="purple"
          stroke-opacity = "1"
          stroke-width = "2"
          stroke-linecap = "square"
          stroke-dasharray = "5,5" />
        <circle cx="10" cy="10" r="2" fill="blue" id="dot2" />
        <text x="10" y="10" id="dot2Text" >(10, 10)</text>
      </svg>
</div>

<div>
    <h1> Toggle </h1>
 
      <label for="dot1XInput"> x1 </label>
      <input id="dot1XInput" class="u-full-width" type="number" min="0" />

      <label for="dot1YInput"> x1 </label>
      <input id="dot1YInput" class="u-full-width" type="number" min="0" />

      <label for="viewBoxXInput"> x1 </label>
      <input id="viewBoxXInput" class="u-full-width" type="number" min="0" />

      <label for="viewBoxYInput"> x1 </label>
      <input id="viewBoxYInput" class="u-full-width" type="number" min="0" />

      <label for="viewBoxWidthInput"> x1 </label>
      <input id="viewBoxWidthInput" class="u-full-width" type="number" min="0" />

      <label for="viewBoxHeightInput"> x1 </label>
      <input id="viewBoxHeightInput" class="u-full-width" type="number" min="0" />
     
</div>
</div>












<script>
// convenient setting functions

var line = document.getElementById('line')
var dot1 = document.getElementById('dot1')
var dot2 = document.getElementById('dot2')
var dot1Text = document.getElementById('dot1Text')
var svgViewBox = document.getElementById('svgViewBox')
var rectViewBox = document.getElementById('rectViewBox')

function setStartX(x) {
  line.x1.baseVal.val = x;
  line.x1.baseVal.value = x;
  document.getElementById('startXCode').innerHTML = "&quot;" + x + "&quot;";
}

function setStartY(y) {
  line.y1.baseVal.val = y;
  line.y1.baseVal.value = y;
  document.getElementById('startYCode').innerHTML = "&quot;" + y + "&quot;";
}

function setEndX(x) {
  line.x2.baseVal.val = x;
  line.x2.baseVal.value = x;
  document.getElementById('endXCode').innerHTML = "&quot;" + x + "&quot;";
}

function setEndY(y) {
  line.y2.baseVal.val = y;
  line.y2.baseVal.value = y;
  document.getElementById('endYCode').innerHTML = "&quot;" + y + "&quot;";
}

function setStrokeWidth(width) {
  line.attributes['stroke-width'].value = width;
  document.getElementById('strokeWidthCode').innerHTML = "&quot;" + width + "&quot;";
}

function setStrokeColor(color) {
  line.attributes['stroke'].value = color;
  document.getElementById('strokeColorCode').innerHTML = "&quot;" + color + "&quot;";
}

function setStrokeOpacity(opacity) {
  line.attributes['stroke-opacity'].value = opacity;
  document.getElementById('strokeOpacityCode').innerHTML = "&quot;" + opacity + "&quot;";
}

function setStrokeDash(dash) {
  line.attributes['stroke-dasharray'].value = dash;
  document.getElementById('strokeDashCode').innerHTML = "&quot;" + dash + "&quot;";
}

function setdot1X(x) {
  dot1.cx.baseVal.val = x;
  dot1.cx.baseVal.value = x;
  dot1Text.attributes.x.value = x;
  dot2.attributes.cx.value = x;
}

function setdot1Y(y) {
  dot1.cy.baseVal.val = y;
  dot1.cy.baseVal.value = y;
  dot1Text.attributes.y.value = y;
  dot2.attributes.cy.value = y;
}

function setViewBoxX(x) {
  svgViewBox.viewBox.baseVal.x = x;
  rectViewBox.attributes.x.value = x;
}

function setViewBoxY(y) {
  svgViewBox.viewBox.baseVal.y = y;
  rectViewBox.attributes.y.value = y;
}

function setViewBoxWidth(width) {
  svgViewBox.viewBox.baseVal.width = width;
  rectViewBox.attributes.width.value = width;
}

function setViewBoxHeight(height) {
  svgViewBox.viewBox.baseVal.height = height;
  rectViewBox.attributes.height.value = height;
}


// Populate initial values
(function() {
  // initial values
  var startX = "15";
  var startY = "25";
  var endX = "145";
  var endY = "105";
  var strokeWidth = "1";
  var strokeOpacity = "1";
  var strokeColor = "black"
  var strokeDash = "5,5";

  //svg drawing


  //code


  //input fields
    document.getElementById('startX').value = 50;
    document.getElementById('startY').value = 25;
    document.getElementById('endX').value = 100;
    document.getElementById('endY').value = 125;
})();


// event handlers 
document.getElementById('startX').addEventListener("input", function(e){
  setStartX(e.target.value);
  document.getElementById('startCoordinates').x.baseVal.val = e.target.value;
  document.getElementById('startCoordinates').x.baseVal[0].value = e.target.value;
  var pres = document.getElementById('startCoordinates').innerHTML.split(',')[1]; 
  document.getElementById('startCoordinates').innerHTML = e.target.value + ',' + pres; 
})

document.getElementById('startY').addEventListener("input", function(e){
  setStartY(e.target.value);
  document.getElementById('startCoordinates').y.baseVal.val = e.target.value;
  document.getElementById('startCoordinates').y.baseVal[0].value = e.target.value;
  var pres = document.getElementById('startCoordinates').innerHTML.split(',')[0]; 
  document.getElementById('startCoordinates').innerHTML = pres + ',' + e.target.value; 
})


document.getElementById('endX').addEventListener("input", function(e){
  setEndX(e.target.value);
  document.getElementById('endCoordinates').x.baseVal.val = e.target.value;
  document.getElementById('endCoordinates').x.baseVal[0].value = e.target.value;
  var pres = document.getElementById('endCoordinates').innerHTML.split(',')[1]; 
  document.getElementById('endCoordinates').innerHTML = e.target.value + ',' + pres; 
})

document.getElementById('endY').addEventListener("input", function(e){
  setEndY(e.target.value);
  document.getElementById('endCoordinates').y.baseVal.val = e.target.value;
  document.getElementById('endCoordinates').y.baseVal[0].value = e.target.value;
  var pres = document.getElementById('endCoordinates').innerHTML.split(',')[1]; 
  document.getElementById('endCoordinates').innerHTML = e.target.value + ',' + pres; 
})

document.getElementById('strokeWidth').addEventListener('input', function(e){
  setStrokeWidth(e.target.value);

})

document.getElementById('strokeOpacity').addEventListener('input', function(e){
  setStrokeOpacity(e.target.value);

})

document.getElementById('strokeColor').addEventListener('input', function(e){
  setStrokeColor(e.target.value);
})

document.getElementById('strokeDash').addEventListener('input', function(e){
  setStrokeDash(e.target.value);
})

document.getElementById('dot1XInput').addEventListener('input', function(e){
  setdot1X(e.target.value);
})

document.getElementById('dot1YInput').addEventListener('input', function(e){
  setdot1Y(e.target.value);
})

document.getElementById('viewBoxXInput').addEventListener('input', function(e){
  setViewBoxX(e.target.value);
})


document.getElementById('viewBoxYInput').addEventListener('input', function(e){
  setViewBoxY(e.target.value);
})

document.getElementById('viewBoxWidthInput').addEventListener('input', function(e){
  setViewBoxWidth(e.target.value);
})

document.getElementById('viewBoxHeightInput').addEventListener('input', function(e){
  setViewBoxHeight(e.target.value);
})


</script>