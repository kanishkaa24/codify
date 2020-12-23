# codify
#Study platform
<!----CODIFY---->
<html>
<head> 
<style>
a:link{text-decoration: none;color:Green;}
a:visited{text-decoration: none;color:pink;}
a:hover{text-decoration: underline;color:red;}
a:active{color:yellow; background-color:transparent; text-decoration:underline}
title
{
	color: red;
}
body
{
        background-image:url("D:\OIP (1).jpg");
        /* Full height */
        height: 100%; 

        /* Center and scale the image nicely */
        background-position: center;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        background-attachment: fixed;
        font: italic bold 13px 'Times New Roman', Times, FreeSerif, serif;
        color: #99b0da;
}
html body .content-outer {
min-width: 0;
max-width: 100%;
width: 100%;
}
.content{
background:white;
width:50%;
padding:80px;
margin-top:0;
margin:100px auto;
}
.content1{
background:black;
width:10%;
padding:10px;
/*margin:100px auto;*/
}
p{
font-size:25px;
}
h1
{
        color:purple;
        background-color:lightsalmon;
}
</style>
<title>CODIFY</title>
<link rel="icon" href="D:\OIP.jpg" type="image/icon type">
</head>
<body>
<div class="row">
			<div class="col-md-12">
				<button class="btn btn-default js-go-day">DAY NODE</button>
				<button class="btn btn-default js-go-night">NIGHT NODE</button>
			</div>
			</div>
			<script>

		$('.js-go-night').click(function(){
			$('body').addClass('night');
			$('div').addClass('night');
			$('li').addClass('night');

		});
		$('.js-go-day').click(function(){
			$('body').removeClass('night');
			$('div').removeClass('night');
			$('li').removeClass('night');
		});


		// this is a variable to keep track
		// of which chapter we are on
		var counter = 0;

		// when we click on a chapter thumbnail
		// it displays that chapter
		// this code is pretty similar to the
		// image gallery, but I've added some code
		// to update the counter
		$(".chapter-thumbnail").click(function(){
			// copy the html from the thumbnail (this)
			// to the main viwer
			$("#mainViewer").html(
				$(this).html());

			// get the id of this element so we can
			// get hold of its number
			var id = $(this).attr("id");

			// set the counter to the number of the
			// chapter we selected.
			// We get this by taking the last charcter
			// of the id and convert it to a number
			// id.slice gets a subsection of the string
			// passing in -1 means we get just the
			// last character
			// parseInt converts it to a number (integer)
			counter = parseInt(id.slice(-1));
		});

		// virtually click the first chapter to select it
		$("#chapter"+counter).click();

		// when we click on the main viewer we want to
		// move forward or backward in the
		// chapter
		$("#mainViewer").click(function (event){

			// move forward if we click to the right
			// or backward if we click to the left

			// event.offsetX is the horizontal
			// position of the mouse inside the
			// element we have clicked on,
			// it will be between 0
			// and the width of the element

			// $(this).width()*0.3 is 30% of
			// the with of the element

			// if event.offsetX is less than
			// 30% of the width, it means it is
			// on the left hand side
			if(event.offsetX
				< $(this).width()*0.3){
				// if we've clicked on the left
				// go back
				counter = counter - 1;
			} else {
				// if we've clicked on the right
				// go forwards
				counter = counter + 1;
			}

			// If we've gone below 0 it means
			// we were at the beginning, and
			// should just stay at zero
			if(counter < 0){
				counter =  0;
			}

			// $(".chapter-thumbnail").length
			// is the number of elements that
			// match the selector .chapter-thumbnail
			// i.e. the number of chapter thumbnails
			// if counter is equal to or more than
			// the number of thumbnails it means
			// we've gone past the last chapter which
			// is $(".chapter-thumbnail").length-1
			// (because we start counting at 0)
			if(counter >=
				$(".chapter-thumbnail").length){
				counter =
			$(".chapter-thumbnail").length-1;
			}

			// we get the id of the chapter thumbnail
			// we want by putting counter on the end
			// of it.
			// we can do a virtual click on the
			// chapter thumbnail to select it
			$("#chapter"+counter).click();
		});

	</script>
<h1><p><b><i><center>CODIFY</b></i></center></p>
<p><center><i>Come and learn coding with us</i></center></p></h1>
<div class="content1"><h2 style="text-align:left;"><b><i><p>Contents:</p>
<p><a href="file:///C:/Users/hp/OneDrive/Desktop/project.html">Home</a></p>
<p><a href="#1">To write a program to insert an element in an array in the given position</a></p>
<p><a href="#2">To write a program to find the area and circumference of the circle</a></p>
<p><a href="#3">A program to check whether a person is eligible to vote or not</a></p></h2></div></b></i>
<div class="content"><div dir="ltr" style="text-align:left;" trbidi="on">
<h3 style="text-align:left;" id="1">
<span style="color: purple;"><b>AIM:To write a program to insert an element in an array in the given position</b></span></h3>
<br />
<div>
<span style="color: orange;">ALGORITHM:</span><br />
Step-1 Start the program<br />
<div>
Step-2 Enter the size of the array</div>
<div>
Step-3 Enter the elements of the array</div>
<div>
Step-4 Print the elements of the array</div>
<div>
Step-5 Enter the element to be inserted and its position in the array</div>
<div>
Step-6 Set a loop up to the position you enter</div>
<div>
Step-7 Push the order of the position by one, which are greater,then the position you entered<br />
Step-8 Insert the element in the position entered by you</div>
<div>
Step-9 Print the array after insertion of the element</div>
<div>
Step-10 Stop</div>
<div>
<span style="color: orange;"></span><br />
<!--more--><span style="color: orange;"><br /></span>
<span style="color: orange;">PROGRAM:</span><br />
<span style="color: red;">/*INSERTING AN ELEMENTS INTO THE VECTOR*/</span></div>
<div>
#include&lt;stdio.h&gt;</div>
<div>
void main()</div>
<div>
{int a[100],no,i,pos,item;</div>
<div>
printf(“\nEnter the size of the matrix”);</div>
<div>
scanf(“%d”,&amp;no);</div>
<div>
printf(“\nEnter the elements of the matrix”);</div>
<div>
for(i=0;i&lt;no;i++)</div>
<div>
scanf(“%d”,&amp;a[i]);</div>
<div>
printf(“\nEntered elements of the matrix is”);</div>
<div>
for(i=0;i&lt;no;i++)</div>
<div>
printf(“\n%d”,a[i]);</div>
<div>
printf(“\nEnter the element and its position in the array”);</div>
<div>
scanf(“%d\n%d”,&amp;item,&amp;pos);</div>
<div>
no++;</div>
<div>
for(i=no;i&gt;=pos;i-)a[i]=a[i-1];</div>
<div>
a[-pos]=item;</div>
<div>
printf(“\n”);</div>
<div>
printf(“\nArray after the insertion”);</div>
<div>
for(i=0;i&lt;no;i++)</div>
<div>
printf(“\n%d”,a[i]);}</div>
<div>
<span style="color: orange;"><br /></span>
<span style="color: orange;">SAMPLE OUTPUT:</span></div><div>Enter the size of the array&nbsp;</div>
<div>
5</div>
<div>
Enter the elements of the array</div>
<div>
1 2 4 5 6</div>
<div>
Entered elements of the array</div>
<div>
1 2 4 5 6</div>
<div>
Enter the element and its position in the array&nbsp;</div>
<div>
3</div>
<div>
Array after the insertion</div>
<div>
1 2 3 4 5 6</div>
</div>
</div></div>
<div class="content"><div dir="ltr" style="text-align: left;" trbidi="on">
<h4 style="text-align: left;">
<span style="color: purple;"><span style="color: #4c1130;" id="2">AIM:</span>To write a program to find the area and circumference of the circle.</span></h4>
<br />
<span style="color: orange;"> ALGORITHM:</span><br />
Step-1 Start the program.<br />
<div>
Step-2Input the radius of the circle.</div>
<div>
Step-3Find the area and circumference of the circle using the formula Area=3.14*r*r and Circumference=2*3.14*r</div>
<div>
Step-4Print the area and the circumference of the circle</div>
<div>
Step-5Stop<br />
<br />
<!--more--><br /><br />
<span style="color: orange;">PROGRAM</span>:<br />
<div>
<span style="color: red;">/*TO FIND THE AREA AND CIRCUMFERENCE OF THE CIRCLE*/</span><br />
<div>
#include&lt;stdio.h&gt;</div>
<div>
void main()</div>
<div>
{float rad,area,circum;</div>
<div>
printf(“\nEnter the radius of the circle”);</div>
<div>
scanf(“%f”,&amp;rad);</div>
<div>
area=3.14*rad*rad;</div>
<div>
circum=2*3.14*rad;</div>
<div>
printf(“\nArea=%f”,area);</div>
<div>
printf(“\nCircumference=%f”,circum);}<br />
<br />
<br />
<span style="color: orange;">SAMPLE INPUT AND OUTPUT:</span><br />
Enter the radius of the circle 5<br />
Area=78.500000<br />
Circumference=31.400000</div>
</div>
</div>
</div></div>
<div class="content"><div dir="ltr" style="text-align: left;" trbidi="on">
<br />
<div class="MsoNormal">
<v:shapetype coordsize="21600,21600" filled="f" id="_x0000_t75" o:preferrelative="t" o:spt="75" path="m@4@5l@4@11@9@11@9@5xe" stroked="f"><b><i>
 <v:stroke joinstyle="miter">
 <v:formulas>
  <v:f eqn="if lineDrawn pixelLineWidth 0">
  <v:f eqn="sum @0 1 0">
  <v:f eqn="sum 0 0 @1">
  <v:f eqn="prod @2 1 2">
  <v:f eqn="prod @3 21600 pixelWidth">
  <v:f eqn="prod @3 21600 pixelHeight">
  <v:f eqn="sum @0 0 1">
  <v:f eqn="prod @6 1 2">
  <v:f eqn="prod @7 21600 pixelWidth">
  <v:f eqn="sum @8 21600 0">
  <v:f eqn="prod @7 21600 pixelHeight">
  <v:f eqn="sum @10 21600 0">
 </v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:f></v:formulas>
 <v:path gradientshapeok="t" o:connecttype="rect" o:extrusionok="f">
 <o:lock aspectratio="t" v:ext="edit">
</o:lock></v:path></v:stroke></i></b></v:shapetype><v:shape id="Ink_x0020_4" o:spid="_x0000_s1027" style="height: 1.45pt; margin-left: 60.9pt; margin-top: 113.9pt; mso-height-percent: 0; mso-height-percent: 0; mso-height-relative: page; mso-position-horizontal-relative: text; mso-position-horizontal: absolute; mso-position-vertical-relative: text; mso-position-vertical: absolute; mso-width-percent: 0; mso-width-percent: 0; mso-width-relative: page; mso-wrap-distance-bottom: 0; mso-wrap-distance-left: 9pt; mso-wrap-distance-right: 9pt; mso-wrap-distance-top: 0; mso-wrap-style: square; position: absolute; visibility: visible; width: 1.45pt; z-index: 251661312;" type="#_x0000_t75">
 <v:imagedata o:title="" src="file:///C:/Users/hp/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png"><b><i>
</i></b></v:imagedata></v:shape><v:shape id="Ink_x0020_3" o:spid="_x0000_s1026" style="height: 1.45pt; margin-left: 41pt; margin-top: 97.2pt; mso-height-percent: 0; mso-height-percent: 0; mso-height-relative: page; mso-position-horizontal-relative: text; mso-position-horizontal: absolute; mso-position-vertical-relative: text; mso-position-vertical: absolute; mso-width-percent: 0; mso-width-percent: 0; mso-width-relative: page; mso-wrap-distance-bottom: 0; mso-wrap-distance-left: 9pt; mso-wrap-distance-right: 9pt; mso-wrap-distance-top: 0; mso-wrap-style: square; position: absolute; visibility: visible; width: 1.45pt; z-index: 251660288;" type="#_x0000_t75">
 <v:imagedata o:title="" src="file:///C:/Users/hp/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png"><b><i>
</i></b></v:imagedata></v:shape></div>
<h5 style="text-align: left;">
<span style="color: purple;"><i><b style="mso-bidi-font-weight: normal;"><span lang="EN-US" style="font-size: 13.0pt;" id="3">AIM: <span style="mso-spacerun: yes;">&nbsp;</span></span></b><span lang="EN-US" style="font-size: 13.0pt;">A program to check whether a person is
eligible to vote or not.</span></i></span></h5>
<div style="text-align: left;">
<b><span lang="EN-US" style="background-color: white;"><i><span style="color: orange;">CODING</span></i></span></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: blue; font-family: &quot;consolas&quot;; font-size: 9.5pt;">#include</span><span lang="EN-US" style="background: white; color: #a31515; font-family: &quot;consolas&quot;; font-size: 9.5pt;">&lt;stdio.h&gt;</span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: blue; font-family: &quot;consolas&quot;; font-size: 9.5pt;">void</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"> main()<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">{ </span></i></b><br />
<!--more--><b><i><span lang="EN-US" style="background: white; color: blue; font-family: &quot;consolas&quot;; font-size: 9.5pt;">int</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"> a;<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><b><i><span style="mso-spacerun: yes;">&nbsp;</span>clrscr();<o:p></o:p></i></b></span></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span>printf(</span><span lang="EN-US" style="background: white; color: #a31515; font-family: &quot;consolas&quot;; font-size: 9.5pt;">"the age"</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">);<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span>scanf(</span><span lang="EN-US" style="background: white; color: #a31515; font-family: &quot;consolas&quot;; font-size: 9.5pt;">"%d"</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">,&amp;a);<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span></span><span lang="EN-US" style="background: white; color: blue; font-family: &quot;consolas&quot;; font-size: 9.5pt;">if</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">(a&gt;=18)<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span>printf(</span><span lang="EN-US" style="background: white; color: #a31515; font-family: &quot;consolas&quot;; font-size: 9.5pt;">"eligible to
vote"</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">);<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span></span><span lang="EN-US" style="background: white; color: blue; font-family: &quot;consolas&quot;; font-size: 9.5pt;">else</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span>printf(</span><span lang="EN-US" style="background: white; color: #a31515; font-family: &quot;consolas&quot;; font-size: 9.5pt;">"not eligible to
vote"</span><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;">);<o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><b><i><span style="mso-spacerun: yes;">&nbsp;</span>getch();<o:p></o:p></i></b></span></div>
<div class="MsoNormal">
<b><i><span lang="EN-US" style="background: white; color: black; font-family: &quot;consolas&quot;; font-size: 9.5pt;"><span style="mso-spacerun: yes;">&nbsp;</span>}</span><span lang="EN-US"><o:p></o:p></span></i></b></div>
<div class="MsoNormal" style="mso-layout-grid-align: none; text-autospace: none;">
<br /></div>
<div class="MsoNormal">
<b><span lang="EN-US"><i><span style="color: orange;">OUTPUT</span><o:p></o:p></i></span></b></div>
<div class="MsoNormal">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a imageanchor="1" style="background-color: black; clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"><img alt="program to check voting age" border="0" data-original-height="103" data-original-width="262" src="https://1.bp.blogspot.com/-tt37e2T5Asg/Xkqgaz4Pu_I/AAAAAAAATdg/uWadOUgvALMVpPNRZJHeHq7yl4KjF2KmwCLcBGAsYHQ/s1600/Annotation%2B2020-02-17%2B194625.png" title="ouput" /></a><b><i></i></b></div>
<br />
<div class="MsoNormal">
<b style="mso-bidi-font-weight: normal;"><i><span lang="EN-US" style="mso-no-proof: yes;"><v:shape id="Picture_x0020_1" o:spid="_x0000_i1025" style="height: 282pt; mso-wrap-style: square; visibility: visible; width: 451.2pt;" type="#_x0000_t75">
 <v:imagedata o:title="" src="file:///C:/Users/hp/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png">
</v:imagedata></v:shape></span><span lang="EN-US" style="mso-bidi-font-weight: bold;"><o:p></o:p></span></i></b></div>
<br /></div></div>


</body>
<!--  Camera_Slideshow Styles  -->
<link rel="stylesheet" id="camera-css" href="http://project.dimpost.com/camera-slideshow/css/camera.css" type="text/css" media="all" />
<!-- Camera Slideshow Scripts -->
<script type='text/javascript' src='https://code.jquery.com/jquery-2.1.4.min.js'></script>
<script type='text/javascript' src='http://project.dimpost.com/camera-slideshow/scripts/jquery.mobile.customized.min.js'></script>
<script type='text/javascript' src='http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js'></script>
<script type='text/javascript' src='http://project.dimpost.com/camera-slideshow/scripts/camera.min.js'></script>
<script type='text/javascript'>
jQuery(function() {
jQuery('#camera_wrap_1').camera({
time: 2500, // milliseconds between the end of the sliding effect and the start of the nex one
transPeriod: 1200, // length of the sliding effect in milliseconds
thumbnails: false, // thumnails & tooltip is controlled by it
pagination: true, // only when "pagination" is set to "false" thumbnails will be visible
fx: 'curtainTopLeft, curtainTopRight, curtainBottomLeft, curtainBottomRight, curtainSliceLeft, curtainSliceRight, blindCurtainTopLeft, blindCurtainTopRight, blindCurtainBottomLeft, blindCurtainBottomRight, blindCurtainSliceBottom, blindCurtainSliceTop, stampede, mosaic, mosaicReverse, mosaicRandom, mosaicSpiral, mosaicSpiralReverse, topLeftBottomRight, bottomRightTopLeft, bottomLeftTopRight, bottomLeftTopRight, scrollLeft, scrollRight, scrollHorz, scrollBottom, scrollTop', // transition effects
hover: false, // Pause on hover
height: '50%' // slideshow height (50% is default)
});
});
</script>
<style type="text/css">
.fluid_container {
margin: 0 auto;
/* aling centered */
width: 100%;
max-width: 900px;
overflow: hidden;
}

/* Blogger CSS Conflict Fix */
.camera_pag_ul {
border: none !important;
background: none !important;
}
.camera_pag_ul li {
float: inherit !important;
padding: inherit !important;
}
.camera_pag_ul {
margin: 0 !important;
border: 0 !important;
}
</style>
<div class="fluid_container">
<!-- camera_slideshow camera_wrap-->
<div class="camera_wrap" id="camera_wrap_1">
<div data-link="YOUR LINK HERE" data-thumb="http://project.dimpost.com/camera-slideshow/images/slides/thumbs/1.jpg" data-src="https://1.bp.blogspot.com/-ztgav987eac/XmOZ50XJkLI/AAAAAAAAUBU/3NPmT02ue8sUg8XfkqyJ_swkpJm5_1KEwCLcBGAsYHQ/s1600/3.jpg">
<div class="camera_caption fadeFromBottom">
Encode</div>
</div>
<div data-link="YOUR LINK HERE" data-thumb="http://project.dimpost.com/camera-slideshow/images/slides/thumbs/2.jpg" data-src="https://1.bp.blogspot.com/-xzb250fDtzY/XmOZ6NtJT2I/AAAAAAAAUBc/65xfJ5mdMuoStMEYcGJ6FoReY4ORwNz5gCLcBGAsYHQ/s1600/2.png">
<div class="camera_caption fadeFromBottom">
Coder's Mind</div>
</div>
<div data-link="YOUR LINK HERE" data-thumb="http://project.dimpost.com/camera-slideshow/images/slides/thumbs/3.jpg" data-src="https://1.bp.blogspot.com/-rrYPhREqD1o/XmOZ6HcpaRI/AAAAAAAAUBY/rJKmaobvYSY92ep7WiI_zT8q9wxrtHIeACLcBGAsYHQ/s1600/1.jpg">
<div class="camera_caption fadeFromBottom">
Computer Understandable Language</div>
</div>
</div>
<!-- #camera_wrap_1 -->
</div>
<!-- .fluid_container -->
</html>
