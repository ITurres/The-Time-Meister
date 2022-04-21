# Personal-Project-1
LANDING PAGE.-

For this project I will be creating a landing page, with the knowledge acquired in The Odin Project foundations CSS-Flexbox-"Project", that you can check in my repositories under the name "The O.P-Project".

It will contain:
*- A navbar with links and a Centered Clickable logo.
*- A header with a large image edge to edge and a Tittle on it.
*- A section with three different text next to three dif images and a button above each text.
*- A Meet the team Section. with an small subtitle, img and a sub info tag.
*- A footer with Address-phones-copyright info,etc.
~~~~~~~~~~~~~~~~~

18/04/2022.-

As usual I will begin with adding a boilerplate onto the index.html file.
then, I will anchor the style.css file.

>

index.html:>

NAVBAR:
       so the navbar will contain the respective items mention above, in order to do that i need to add a html tag, in this case a nav class to hold a div of Logo for the logo and a unordered list class under the name of "nav" for the links.
       Also, I believe under what i think its right, that in order to have my logo centered and two of the links to the left and two to the right; on index. I have to write the first two links, then the logo and then, the last two links. For them to be as mentioned. 

HEADER:
       For the header i will need to add a header tag with a class of header to hold the img and the tittle. (THE THING WILL BE HOW TO WRITE THE HTML FILE SO THE TITTLE GETS ON TOP OF THE IMG): RESOLVE.> 
       
       Solution: 
       > HTML: will need a container
       then a div with class with the text in it.
         
       > CSS: for the "container" give a property of position:relative.
       For the item (text in image) give a property of position:absolute, top:50% and left:50% and transform: translate(-50%, -50%);.
       IMPORTANT: all thi will work, but will affect the navbar, causing this to disappear under the image with text. (TO BE RESOLVE)...
       
SECTION: 
        In the case of the Section, I will open a section tag with the same name of class, then under it will go a class of container and its child will be a class of items.
        Then, ill <div> texts, images and a button for each one of the items.
        *-The idea is, to have some text on the LEFT, right to the text the image and below the text will go the button. (same for all items).

SECTION-2: 
          On the other hand, this section will only hold a small tittle, under it, will be an image and below it will go a small text.
          *- The idea in this case will be to have the image centered in the container, with the tittle in bold on top and the small text on the foot of the image.       

FOOTER: 
       The footer will hold the "copyright" stamp and 3 items (three), one of them a link.
       The idea: 2 non-links items on the LEFT, the stamp will be centered and the item with the link on the RIGHT.

>

style.css:>

As a start, I will five some general properties (*) to the whole page. boz-sizing-padding-and margin
then I will add some properties to the <body>. also I will add flexbox to body so  it will push the footer to the bottom.

NAVBAR: 
       after given some background color,a font color and a height, i will start giving properties to <nav> class into the navbar.

IMPORTANT!!> I had troubles finding out how to edit the HTML in order to get two links on the left, the logo centered and two more links on the right. But after playing around and consulting stack overflow, I found this possible solution that at the moment is working fine.

SAVE THIS SCHEME FOR FUTURE REFERENCES:

<div class="navbar">
    <nav>
            <div>
                <a href="*">LINK NAME</a>
                <a href="*">LINK NAME</a>
            </div>
        <div id="logo"><a href="home">LOGO NAME</a></div>
            <div>
                <a href="*">LINK NAME</a>
                <a href="*">LINK NAME</a>
            </div>
    </nav>
    </div>
>
This will do.


19/04/2022.-

NAVBAR:

Today I will continue working with the navbar, i want to set the .navbar on top of an image in .header, as well as give some hover color to the links.

>After a short research online, i couldn't find an answer, but!, after playing around with css, i realized that in order to do what i need, i have to add a property call> -Position: absolute- TO the navbar class (NOT TO THE HEADER CLASS), so this goes on top of the image that was below. 

After doing this, the navbar will lose its auto width, so in order to have it taking all the space available, will need a width property of 100%. Also add a width of 100% to img so it takes all the screen available as wanted.<

HEADER:
       Now that the navbar is on top of the image, i need the h1 title to go on top of the .header image and be centered.
       
!>PROBLEM TO BE RESOLVE: (regarding the centered text in image in header): when I give the position:relative property to my .header class, it makes the navbar (which has property:absolute) disappear under the .header image. so i need to find a way to center my text in the image and both to be under my navbar.

21/04/2022.-

SECTION: in every section that has a .container class will have a max-width of 1100px and i will give a margin to it... 0 for top and bottom and auto for left and right, so it will be centered.

*-the section class will have a background color.
and the section img will have a max-width and padding to the left.

*-now the container within it, i will add flexbox and wrap, so i can have the items stack. Some margin will be applied to the container as well.

*-Regarding the items within it, they will need a background color, align text, some padding to give space to the img and text, some properties to the button and font properties.
Item (2): i want this item in a different order, the img on the left and text-button on the right.to achieve this, apply the "flex-direction: row-reverse" property and modify padding values.

*-Button: i want them to be away from the text and img, black and without border.

the last style will be to border-radius the image and item containers.

SECTION-2:
          For this section, the background will be a light gray. i will need to edit the html a bit so when i add flexbox to the container the h1-img-h3 won't be in a row...OR ADD flex-direction: column> to the container will keep them stack. 