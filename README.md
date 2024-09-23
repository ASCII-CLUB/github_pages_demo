# ASCII-CLUB.github.io
Step 0: Github Account
At this point, everyone should have a GitHub account. They should be able to push and pull from VSCODE or gitbash, and have access to the ASCII-CLUB Github.

If you do not have a Github account, go ahead and create one using a personal email address. Do NOT use your school email address, as you will have to change this later down the road.

For this meeting, we will be using VSCode and HTML/CSS to develop a site for your personal github. It is important that you have these things downloaded: 

The VCS, Git - https://git-scm.com/downloads 
The IDE, VS Code - https://code.visualstudio.com/download  

With GIT installed, link your github and git via HTTPS key. This is important, as you will need to be able to do this for anything to work during this workshop.

Once you have VS Code, install these extensions from the extensions tab.

Live Server Extension - install this on VScode extensions
https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer 

HTML CSS -  install this on VScode extensions
https://marketplace.visualstudio.com/items?itemName=sidthesloth.html5-boilerplate


We will be doing all of this or helping those who werent able to during the club meeting. Having atleast the extensions and programs downloaded will make everything go smoother :) 
GITHUB, VSCODE, HTML EXTENSIONS

Step 1: Creating the Github Repository
Navigate to GitHub, and create a new repository. Do NOT create this in the ASCII-CLUB github. Create this in your own github. You can find this by clicking on your profile banner and clicking
“Your Repositories”.
	










Once you are to this point, click the green ‘new’ button. Name this repository [yourgithubusername].github.io.
The letters in this username should be lowered cased.


In order for this to be a successful github pages site, you need to have this exact format for the name of your repository. You can choose between public and private but regardless of what you choose your site will be public for anyone to find.

You can initiate this with a READ.md file if you would like. Go ahead and create the repository.

Navigate to your repository. Click ‘Settings’ and navigate to Pages. 
Build and Development should be selected as Deploy from a Branch, and Branch should be on Main. You can click ‘Visit Site’ to view your very simple site!
Repository is Created and Github Pages works

Step 2: Pulling from Github and Index.html
In order to add something to your github pages, you will need to add a file called index.html. Github pages automatically adds your README.md file as your entry file, but will also search for an index.html or index.md for an entry file. 

To add this file, we will need to pull from github. If you have your VSCode and Git credentials stored, this will be very easy. Simply navigate to a directory where you want to store your repository, and 
$ git clone [repository URL]









You should  see something like this:
Cloning into 'ASCII-CLUB.github.io'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.

Perfect! Now that you are at this point, you can directly work on the main branch. You should never directly work on main. For this workshop, we will be directly working on main, for convenience sake. 

Go ahead and create your index.html.

For this workshop, we will be creating a very basic about me section for your github page. You can have coding experience on here, a short description about yourself, or really whatever else you want. We will use HTML, and then use a template CSS file to stylize your page. 

Before we move to creating your site, add 3 three things to your html file.
<!DOCTYPE html>  	<!-- specifies documentent type-->
<html>			<!-- where the html document begins -->
    <body>		<!-- the 'body' of the file, where your content will be -->



    </body>
</html>






These three items you just added are called ‘tags’ These are the structure of the document, and form elements once you store something between these tags. They are the basis of HTML, and will need to be used in every HTML file you create.

HTML is not a coding language, but rather a markup language.
HyperText Markup Language

Go ahead and add a new <p> tag within your body tags, and add some content between those tags. Now click ‘GO LIVE’ in the bottom right corner of your VSCODE.

<!DOCTYPE html>  	<!-- specifies documentent type-->
<html>			<!-- where the html document begins -->
    <body>		<!-- the 'body' of the file, where your content will be -->
	<p> Hello WORLD! </p>	
    </body>
</html>



You should now see ‘Hello World!’ on your blank site.


Step 3: About Me Information!
Lets create a short introduction to you. Here you can list your coding experience, fun facts about yourself, aspirations, whatever you want to really. We will add a header, and add an image to give a face to the description!

We will also add a few new tags. 
<main></main> // This is the main tag, it will be a child of the body element. This is where the ‘main content’ will be. It is not required, but helps distinguish what’s most important.

<img src=’./directory/file.png’>  // This is the image element, with the src being the images location relative to your index.html

Self-Closing Tag List

<h1>Header</h1> // This is a header in HTML. It will format your text into a header, giving more emphasis to the text at hand.


<!DOCTYPE html>
<html>
    <body>
        <main>

        <h1>WELCOME TO ASCII!</h1>

        <p>
           	Welcome to the ASCII GitHub!
This is a site for all things related to 
           	ASCII Club at Appalachian State University! 
We do coding projects, have speakers,
            	events, and more!
        </p>

        <img src="./images/ascii.jpg">

        </main>
    </body>
</html>




Finalized Code! The Result. Looking pretty ‘meh’, in my opinion.




Let's make it look pretty. We will be using CSS, or cascading style sheets for this. CSS is also not a programming language- but rather a markup language used to style html.

Go ahead and create a new file called style.css.
I want to change the body element- so I will create a ruleset.

style.css :
body {
    background-color: white; /* I want to change my background color */
    margin: 50px; /* outter margin for my body */
}

h1 {
    font-size: 7vw; /* font size for header is 7 vw (vw = 1% of viewports width)*/
    margin-bottom: -3px; /* remove margin from bottom */
}

p {
    font-size: 4vw; 
    margin-top: -5px;
}

.box {
    background-color: #2F3C7E;
    border-radius: 10px;
    border-color: #2F3C7E;
    color: white;
    padding: 20px;
}

.border {
    border: 10px solid;
    border-color: black;
    border-radius: 5px;
    width: 40vw; 
    height: auto; 
}

.columns {
    flex-direction: column;
    display: flex;
    width: fit-content;
}

.column {
    flex: 70%;
    margin: 10px;
}

.mainFont {
    font-family: Arial, Helvetica, sans-serif;
}

@media (min-width: 768px) {
    .columns {
        flex-direction: row; 
        align-items: flex-end; 
    }
}






























HTML:

<!DOCTYPE html>
<html>
    <link rel="stylesheet" href="style.css">


    <body>
        <main>


        <h1 class="mainFont">WELCOME TO ASCII!</h1>

        <div class="box columns">
            <div class="column">
                <p class="mainFont">
                    Welcome to the ASCII GitHub! This is a site for all things related to 
                    ASCII Club at Appalachian State University! We do coding projects, have speakers,
                    events, and more!
                </p>
            </div>
            
            <div class="column">
                <img class="border" src="./images/ascii.jpg">
            </div>
        </div>



        </main>
    </body>
</html>







Final Result: 


