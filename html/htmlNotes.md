# HTML Notes

HTML stands for Hypertext Markup Language.
It is called a markup language because it uses tags to “mark” content, telling the browser how to display it.

HyperText refers to the ability to connect documents using links.
It allows navigation:
    Within the same page
    Between different pages
    Across different websites

#We can also preview our page with option "Show Preview" instead of using live server again and again.

First Website:
The first website was created at CERN: http://info.cern.ch/hypertext/WWW/TheProject.html
At that time:
    There were no search engines
    Users had to manually navigate using links


# Headings: 
we have different kinds of headings: from <h1> to <h6>
<h1> doesn't just mean that it is the largest text, we can change that in CSS, all these headings have semantic meaning; which say that h1 has the highest priority among all.
One page can only have <h1> heading. Multiple <h1> headings beat the purpose of the priority. 

We must use the heading tags in a sequence: h1(main heading) -> h2(sub-heading) -> h3 -> h4 -> h5 -> h6.
It helps in SEO (Seach Engine Optimization), that means it will not have to read out the whole content, it can just understand from headings that what topics are covered and what not.

    When you search something on google (say, Array) it shows you various website links where you can get to know about arrays, it happens because of this only (using priority of the headings).

# Paragraphs:
Writing the content of the page.
If you write lorem in the <p> tag, it will gerenate a paragraph of some random words. lorem50 gives you paragraph of 50 words.

# difference between tag and element:
A tag is a keyword enclosed in angle brackets (< >) that defines the type of content.
An element is the complete structure, consisting of:
    Opening tag
    Content
    Closing tag
For examples <h1>Hellow World</h1> is a whole element while <h1> is the tag and Hello World is the content.

Some tags do not wrap content and therefore:
    Do not require closing tags
If we want to draw a horizontal line on your webpage , you use a self closing tag <hr>
If we want to put space after a paragraph of a line then we use <br> tag. 

# Lists:
you can directly put number of <li> tags using commands li*(number of list items you want to add)
1. Ordered list : shows the list items with numbering. (default - 1.,2.,3.)
2. Unordered list : shows the list items in bullet points. (default - filled circle)
3. Nested list : Lists inside lists, Used for hierarchical data

# comments:
We can put comments in the html file using this syntax <!--This is a comment-->
This will not be shown in the output, just written for your own understanding.

# anchor tag: <a>
we use href with it which stands for hypertext reference, you put the link you to open and outside you put the text where you write the text on clicking of which the given link will open.
target = _blank here refers to that the link will open in a new tab

# attributes: anything present inside the tag
like we use in achor tag 'href', it gives the property

# image tag:
you can add images in the web page, attributes used are height, width, src, alt

# tables: 
data stored and represented in tabular form
we use <table> tag
tags used in table: tr (table row), th(table heading), td(table data), thead, tbody, tfoot
thead, tbody, tfoot will not change anything in the table bu gives a professional look to the code
attributes involved: colspan, rowspan, border

# file path: 
examples: when you want to insert an image in your web page, you can save the image file in the same folder as your code and put that in the src attribute of the img tag so it can follow the file path and get access of the image so you can add it in your web page.
types of file path:
1. relative path (give the path from th current location)
    suppose a person wants to go to chandni chownk from dwarka 
    when you give directions, you may say start from : here > cannaught place > vikaspuri > chandni chownk

    now when you have to do this process in a code editor for your files, how you can represent in the src is: dwarka/cannaught place/vikaspuri/chandni chownk
    we can also use ../

    Current Folder
          ↓
    Go inside → folder/
          ↓
    Go back → ../

2. abolsute path (give the actual path starting from zero)
    absolute path would be when you say:
    there's earth > asia > india > delhi > chandni chownk 

    in code editor, you giv direct link of the image suppose you want to add.
    in windows: C:\Users\JohnDoe\Documents\Report.docx
    in (Linux)mac: /Users/JohnDoe/Documents/Report.docx

    if you use this, your main file can be erased by someone because everyone can access it now
    browser makes sure this doesn't happens

# boiler plate code :
if we do not use boiler plate code aqnd just directly go with <h1> hello world </h1> , the browser will guess which version of html to use, which is not recommended and can also be harmful for the SEO.
browser never gives an error

<!DOCTYPE html> <!--This is a simple HTML5 document -->
<html lang="en"> <!--This is the root element of the HTML document, and it specifies the language as English -->
    
<!--head tag contains metadata (data about data)--> 
    <head>
        <meta charset="UTF-8"> <!--This specifies the character encoding for the HTML document, which is UTF-8 in this case -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
        <!--This meta tag is used to control the layout on mobile browsers. 
        It sets the width of the viewport to the width of the device and the initial zoom level to 1.0 -->
        
        <title>Document</title>
    </head>
    <body>
        <h1>Hello World</h1>
    </body>
</html>

utf-8 is a library in which there is a binary code for every single character present in the code.
ascii - 1 byte
utf-8 - 1,2,3,4 bytes, it is flexible
    
# div: 
container
it is like forming a container where we can just write the styling we want to do once and for all instead of writing it again and again

# class & id:
class- you can group elements to apply styling on them
    to select a class in external css for styling: .class
id - unique identifier for different elements
    you can name multiple elements with same class but cannot give same id to different elements

# Semantic tags provide meaning to the structure of a webpage.
Examples:
    Header → top section
    Main → main content
    Footer → bottom section

    Why They Matter:
        Improve SEO
        Improve accessibility
        Make code easier to understand

# forms:
like login/signup pages: 
    name:
    age:
    email:
    password:
using the tags:
    <form>
    <input> - specifies you are giving input in the name, say for 'name'
    <label> - specifies what you have to write in that particular placeholder
        like name:___________, here "name:" is the label
    <textarea>
    <select> - for when you need to create a dropdown list select options
attributes:
    ->type - text, number, password, submit, radio, checkbox, date, file, dropdown
        -->after you click submit, this information you filled in the form goes into the backend so it can be stored in the database.
        --> it is stored in the form like that of an excel sheet. Means it stores in tabular form.
        --> say there comes a user who only filled some values and left a column, say 'name:' , 
        how will database understand which value is to be filled in which cell.
            -> hence, the information is sent in a way:
                userName = abc
                userFName = xyz
                userAge = 16
                userPassword = wfdhjks
            
            these are what's called name,value pairs represented like: name = value.

        -->when you put say 3 radio buttons for gender check:- male, female, and other.
            you may notice that in your form, it can select all 3 options at the same time, which is not the right practice.
            -> but once you introduce the 'name' attribute along with 'input type' you will observe that it can only select one of these 3 values.
    
    ->name - it specifies with what name your data will be stores in the database.
        earlier the link was: http://127.0.0.1:3000/html/forms/21_forms.html?
        ->after submitting, link becomes:- http://127.0.0.1:3000/html/forms/21_forms.html?userName=abc&userFatherName=xyz&userAge=16&userPassword=wfdhjks
            -->this information will go to the backend.

    -> for & id:
        for is put with label and id is put with input, it shows that the 'label' and the 'input' are connected to each other.
            what happens with this is, when i click on 'Male' in the form other just clicking on the specific radio button, it can still check the 'Male' box.
            -> now if i fill the form, it generates the link as:
            http://127.0.0.1:3000/html/forms/21_forms.html?userName=abc&userFatherName=xyz&userAge=16&userPassword=dwjhdwe&gender=on
                >>it shows gender = on, instead of gender = female, so how will the backend understand??
                hence, we also put the 'value' attribute.
    
    ->value:
    by putting the value, we get the link: http://127.0.0.1:3000/html/forms/21_forms.html?userName=abc&userFatherName=xyz&userAge=16&userPassword=sxbhjabsa&gender=female

        ->checkbox:
        for when you want to select multiple options in your form at the same time.
            link becomes:
            http://127.0.0.1:3000/html/forms/21_forms.html?userName=abc&userFatherName=xyz&userAge=16&userPassword=dsvfdv&gender=female&Subject=Automata+theory&Subject=Statistics

    ->placeholder
    
# <media> tag:
to integrate video, audio, images, youtube video with your website
attributes for <audio> and <video>:
    src - > connecting the link of the audio/video file
    controls -> to give the website access to out audio/video file.
        -> but this is not the most efficient method to integrate audio/video
    autoplay

# how can you embedd a youtube video into your website??
    <iframe> tag:- we remove the watch?v= part and place embed/
    another way is when you paste it using "share" on youtube, just add embed and do not remove anything.
    