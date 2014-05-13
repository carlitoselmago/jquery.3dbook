Jquery 3d.book plugin 
v1.0
22-01-2014

Carlos Carbonell
carlos.awesomenesss.eu

DEMO
http://awesomenesss.eu/public/Jquery.3dbook/

INSTALL

Move the "3d.book" folder to your root or "js" folder
Remember configure the default options like the placement of the blank.png file that will be used to fill the book inside.
Load the jquery and the 3d.book files
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js"></script>
<script src="3d.book/jquery.threeD_book.js"></script>

Put the book image inside a div and use a class 
 <div class="book" pages="320" hoverfactor="6" onclick="location.href='theurlyouwant';">
        <img src="yourimagehere.jpg" height="237">
 </div>

As you see you can edit the book's settings individually. You can also set the configuration for the defaults.

Call the plugin:
$(".book").threeDbook();


CONFIGURATION

If you want to edit the default values you can enter an array with the settings, this is all the settings and their defaults:
 $(".book").threeDbook({
            generalPerspective: 400, //You can play with this to go till something that looks isometric
            pagesSimulateFactor: 2, //This creates the balance between the real pages and the bogus ones to have a sense of reality with a light browser memory ussage
            pagesDefaultAmount: 150, //If you cannot acces each book's real number of pages this will be the default
            pagesSimulateSpace: 2, //This one works also for simulating the space
            rotationY: -15, //Rotation in the Y axis, you can use this value for more depth simulation
            rotationZ: 0, //Vertical rotation
            translateZ: 0, //This has to do with cover-insidepages 3d margin
            classBlankPage: 'blankwhite_page', //The class that will be added to the "img" blank pages inside
            blankPageSrc: '3d.book/blank.png', //The img that will be used for the inside pages, change this if your pages are not white or you want to add some texture effect
            hoverEffect: true, //Activates or deactivates the hover effect
            easetype: 'all 200ms ease', //The animation values for the hover effect
            perspectiveOrigin: '0% 100%', //Change this if you have issues in relation with other CSS of the page
            transformOrigin: '0% 0%', //Same as last one
            pageShadow: '1px 1px 3px 1px rgba(1,1,1,0.1)' //You can modify the shadow of the pages
          
              });

KNOW ISSUES

Chrome has a weird animation when page is loaded
You may find some issues regarding the impact of this plugin with your page's CSS specially if you already use some CSS3 perspective
The plguin may have a unspected behaviour with books that have thick gramage on their pages, working on a fix for this.
Add your own.

