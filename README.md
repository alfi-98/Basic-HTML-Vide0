# 🚀 Basic-HTML-Video

## ✨ This is a basic walkthrough documentation of how to show video on an html web page. 

💡 This is an extension of Basic-HTML-Login-Form repo. The code is available here: 
```https://github.com/alfi-98/Basic-HTML-Login-Form```

### 1. Folder Structure:
```
Basic-HTML-Video
        |----about
        |       |--about.html
        |       |--about.css
        |        
        |----courses
        |       |--courses.html
        |       |--courses.css
        |
        |----documents
        |       |--documents.html
        |       |--documents.css
        |
        |----landing_page
        |       |--landing_page.html
        |       |--landing_page.css
        |
        |----video
        |       |--video_player.js
        |       |--videos1.mp4
        |
        |----index.html
        |----style.html
```
### 2. Linking the Login Page with landing page:
- In the index.html file we have a submit ```<button>``` which is wrapped inside a ```<a>``` tag.
- The <a> tag redirects the index.html to the landing_page.html
```
<a href="landing_page/landing_page.html"> 
        <button type="button" id="submit" class="submit-button">Click Me!</button>     
</a>  
```
### 3. Landing Page
- At first we create the navbar for routing to different pages. So we include a ```<div>``` tag inside the ```<body>``` of our ```landing_page.html``` file.
```
  <div class="topnav">
    <a href="../landing_page/landing_page.html">Home</a>
    <a href="../documents/documents.html">Documents</a>
    <a href="../courses/courses.html">Courses</a>
    <a href="../about/about.html">About</a>
  </div>
```
- The page will look something like this: 
<img width="1284" alt="Screenshot 2022-11-09 at 11 52 30 AM" src="https://user-images.githubusercontent.com/66726759/200897088-f35e103b-da7c-4d87-91ae-38b091eaa377.png">

- Now to style this page we will link the ```landing_page.css``` file with our ```landing_page.html``` file using the below code:
 ```<link rel="stylesheet" href="landing_page.css">```
- The css code for the styling of the navbar is given below:
```
  .container{
    margin-left: auto;
    margin-right: auto;
    display: block;
    text-align: center;
    padding: 30px;
    background-color: rgb(75, 75, 248);
}
  .topnav {
    overflow: hidden;
    background-color: rgb(255, 255, 255);
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: center;
   
  }
  
.topnav a {
    float: left;
    color: #000000;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
  }
  
.topnav a:hover {
    background-color: #1687ff;
    color: rgb(255, 255, 255);
  }
  
.topnav a.active {
    background-color: #1687ff;
    color: white;
  }

h1{

    font-family: 'Menlo', sans-serif;
    color: white;
  }
```
  




