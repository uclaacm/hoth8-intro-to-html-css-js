# hoth8-intro-to-html-css-js
Starter code from Hack off the Hill 8's intro to html/css/javascript 1 hour workshop.

## Basic Development Environment Setup
Make sure you have Google Chrome and a proper text editor. 
There is no one editor that is best, everyone has their own personal preference. The most commonly used ones are VS Code, Sublime Text, and Atom.

# HTML
HTML(Hyper Text Markup Language) is a fancy way of saying text with extra tags that describe the structure and the content of a web page. Historically, HTML was much more limited, but is now able to do much more, such as images. Hypertext refers to text that can be linked to other text (a link). Lets get started with some HTML!

## HTML Setup
1. Make a new folder.
2. Open the folder in VSCode or your text editor of choosing.
3. Make a new file.
4. Save the file as index.html. Make sure to save the file in the folder you just created.

### Add the following code to the top of your HTML document:
```
/*This lets the browser know that this document is an HTML document. 
Code is just instructions to give to the browser, which runs the code and outputs something that you can see, 
so the browser needs to know that this is an HTML document. */
<!DOCTYPE html>
//This marks the beginning and end of the HTML document. Notice that most tags have an opening and closing
<html>
//This is where you put instructions that are not actually shown on the main part of the page. For now, it needs a title.
  <head>
    //This title tag defines a title for the page used in the browser toolbar and search results.
    <title>Landing page</title>
  </head>
  //The body tag surrounds all visible content on the website. Everything you see will be inside here.
  <body>
    //This is where everything will go!
  </body>
</html> 
```

### Tag: Header
``` <h1>Hello World</h1> ```

- As you can see, putting the header tag around our text makes it look like a true header. By putting our words in the h tag (which stands for header), we are telling the
browser that this piece of text is a header. Knowing this, the browser can apply the header styling to the text. 
- A header tag can be from h1-h6, where the larger the number is, the less important the text will be. Therefore, using a larger number will make the text smaller.
Typically, all of the h tags are used to express section headers and other important information.

By the way, lines and spaces don't matter in HTML. No matter how many new lines and spaces we have, the spacing will remain the same. However, its still important to have good
indentation and spacing practice so your code is easily readable.

### Tag: Paragraph
```<p>This is where the paragraph goes!</p>```
- Pretty self explanatory, this is where you can put blocks of text and sets of normal words that aren't special enough to be headers.

### Tag: Image
``` <img src="url link" height="300"> ```
- Use the img tag to insert an img
- Luckily for img tags, there is no closing tag. Not all tags have one!
- Tags can have attributes. Specifically to the img tag, the src attribute of an image allows you to provide a URL to the image, which can be local or online. The height
    attribute specifies the image height. If the width isn't specified, the image will automatically scale.
- If you want to add an image locally, move your image to the same folder as your index.html file and put the image name as the value for the src attribute. You could also
    copy the local path to the image as use that as src.

### Tag: Ordered List
```
<ol>
  <li>First ordered list item</li> 
  <li>Second ordered list item</li>
</ol>
```
- Note: There are also unordered lists with the tag ```<ul>```. Items in the list are still marked with <li>.
  
### Tag: Button
```
<button>Click Me!</button>
```
- Right now, our button doesn't do anything, but we can make it do something after adding JavaScript!

### Tag: Links
```
<a href="http://acm.cs.ucla.edu/">ACM Website!</a>
```
- The href attribute specifies the URL, the part in the middle is where we write the words that can represent the link

### Tag: Inputs
```
<input types="text" placeholder="input stuff here">
```
- The ```<input>``` tag is used to gather input from users
- The type's attribute specifies the type of input. It can be "text", "number" or "submit" based on what you want the user to input.

### Tag: Line Break
```
<br>
```
- Perhaps the most important of all, the line break tag allows us to separate different elements on our website by more than one line. Vitally important.

# CSS
- The code we have in our HTML file should only represent the content of our webpage. A different language called CSS (Cascading Style Sheet) is used to create
    the rules about the styling of our content.
- With CSS, we can create rules like, "This text should be red" or "There should be x amount of space between these two elements" or "This navigation bar should 
    remain at the top of the screen.
- In reference to cascading, we will discuss it more later. It refers to the rules that are followed when one element is manipulated by multiple CSS styling rules.
```
body: 
{
  color: red;
}
```
- "body" is the selector, which means that this is the html tag you are referring this style to
- "color" is the property you are setting, meaning that this is the aspect of the elements that you are modifying. Every element has some default values.
- "red" is the value that you are setting the property to

## Creating and Linking your HTML File
- Create a file named style.css and save it to the same folder as your HTML file
- Then, add the following line to your HTML file in order to link the two files:
```
<!-- Inside the head tag -->
<link rel="stylesheet" type="text/css" href="style.css">
```
- The href file name must match the name of your file. Our web browser needs to know where to look in order to find our styling, so we need to link our CSS file to our 
    HTML file.
- You can also directly put all CSS code into your HTML file instead by putting it in a <style> tag, but this is not recommended because separating them into two files is
      much cleaner and is the convention. Basically, your code will be much easier to read and modify.
  
- There are many different CSS properties and if you're not sure what property name to use or how to set its value, Google is your besst friend!
    - For example, if I didn't know how to align my text, or say I wanted to align it in the center or to the right instead of the left, I could solve my problem by
        looking up "align text css". The first thing that pops up is the property text-align and some cool examples of it.

## Class and ID in CSS and Their Differences
- Whether they are clearly stated or not in our code, all HTML tags have CLASS and ID attributes
- In CSS we can change these classes and ids in order to manage our styling and style multiple objects in the same way. 
- ID's begin with a "#" and Classes begin with a "." when declaring our styling
- It's also important to notice that when at the same level, the style for ID's overrides the style for classes.
  - This is one part of the "cascading" nature of CSS (Cascading Style Sheets)
   - The reason for this is that ID's were created to be the identifier for one single element, while classes are meant to be for multiple elements.
- This is useful if we have multiple of the same elements that we want to style the same way, but one of these elements needs to stand out in some way
    (We have 10 cows that all have the same traits but one is super cool and we also want it to be pink. So we have the css class for all cows, and the id for the pink cow as well.)
    
- Here is another useful element for our CSS Styling:
```
*{
//changing style stuff
}
```
- Using * allows us to select everything and modify it

- When you are looking for specific colors, look up "Color Picker Online" and you will find the hex color codes for your desired color. Then, you can paste them right into CSS.

## A Couple More Useful Properties
#### Text Properties
  - ```text-align``` defines how the text is aligned
  - ```font-weight``` defines how think of thin the text is going to be
#### Formatting Properties
  - The ```padding``` property is used to generate space around an element's content, inside of any defined borders
  - The ```margin``` property is used to create space around elements, outside of any defined borders
  - Note the difference between the two. Padding adds space to the inside of the element, while margin adds space as a pad on the outside of the element
  
  
# JavaScript
- If we want to make our website more interactive, we need to be able to change the web page through programming and set rules about what will happen given that 
    certain events occur.
- This brings us to our final topic of the day, JavaScript!
- For example, if we wanted to change some text or the display of an image after a button is clicked, we would use JavaScript.
- Changing something about our webpage based on a particular event or condition is often called "Manipulating the DOM"

## But What *Is* the DOM?
- DOM stands for Document Object Model. The DOM is a representation of the page as an object.
- Our HTML source code turns into the DOM, which is the actual document object that models what our webpage should look like. This means that our code and the result produced by
    our code are different, and their distinction is important.
- We can take a look at the DOM of a website by left clicking on the page, and clicking "Inspect"
    - You will notice that what you see looks exactly like HTML. However, this is not our HTML source code that we wrote, this is the DOM. Once our webpage is displayed in
        our browser, we can't change the HTML source code anymore through the browser. We can, however, change the DOM.
- We can change some of the text displayed through manipulating the DOM using Chrome's "Inspect Element". Click the box with the cursor in the upper left corner, then 
    click the element on the page that you want to chagne. Lastly, double click the highlighted and type something out. Our DOM Manipulation should show up on the page.
    - Once we refresh it, the changes will disappear. This is because we changed the DOM, and not the source HTML code. Refreshing uploads a fresh copy of the source.

## So, Where Does JavaScript Come In?
- Manipulating the DOM through Chrome Developer tools is fun for silly pranks, but we want to get in to the real thing. The way you will take your webpage and make it 
interactive is through a language called JavaScript, where we can change text, colors, images, and anything else the our document object that is represented as 
a whole by the DOM. 
- We can also run JavaScript in the console of Chrome Developer Tools! The console allows you to print the value of variables, as well as many other things. 
The function getElementById allows you to get a particular element from the DOM based on its id. The attribute onclick of an element can be set to a function 
that determines what happens when the element is clicked. The attribute innerHTML refers to the text between the tags of an element. In this case,
we are setting the onclick attribute to a function that sets the element with id 'acm-title' to have the text of 'Secret message'

## Key Takeaway
- These concepts may be confusing, but the most important thing to takeaway is a general idea of how JavaScript looks and a general understanding of how it can be used 
programmatically change a webpage.

## Let's Write Some JavaScript!
- The first thing we have to do is create a file named script.js in the same folder as our HTML and CSS files.
- Then, add this code to your HTML file
```
<!-- Inside the body tag just before the closing--> <script src="script.js"></script>
```
- Similar to CSS styling, you can also put all of your JavaScript code within the <script> tag and put it in your HTML file, but again, this is not recommended
  
### Our function:
- In script.js:
```
var clicks = 0;
function myFunction() {
  clicks += 1;
  document.getElementById("clicks").innerHTML = clicks;
}

HTML Portion:
<button type="button" onClick="myFunction()">Click Me!!</button>
<p>Clicks: <p id="clicks">0</p></p>
```
- The () => {} syntax is a fancy way to declare a function in JavaScript
- Document is a global variable that is used to represent the DOM
- Basically, when the button is pressed, our function will be called. And in our function, the variable clicks is incremented, and is then set as the
    inner HTML value of the element with id "clicks", which is right under our button


### That is all for today, thank you so much for listening and I wish you luck in your HOTH 8 experience!
