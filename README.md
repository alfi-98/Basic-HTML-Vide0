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
### 3. Landing Page Navbar:
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
        
💡 After applying the above code we can see that whenever we hover over the navbar options, the background-color and font color of that option gets changed. The code responsible for this change is:
 ```
  .topnav a:hover {
    background-color: #1687ff;
    color: rgb(255, 255, 255);
  }
 ```
 
 ### 4. Showing video on the web page:
   - To show video on the web page we need to use the HTML <video> tag.
   - The html code for showing the video is:
   ```
    <div class="videos">
        <video id="video1" width="400" controls>
                <source src="../video/video1.mp4" type="video/mp4">  Your browser does not support HTML video.
        </video>
    </div>
   ```
   👉 - At first we need to save a video in the ```video``` folder of our project folder. 
      - To style our <video> we have wrapped it inside a ```<div>``` tag which has a ```class``` attribute with value "videos". 
      - The code for the above procedure:
        ```
        .videos{
    
            width: 400px;
            height: 200px;
            border-radius: 10px;
            overflow: hidden;
            margin-left: auto;
            margin-right: auto;
        }
        ```
   - Our landing page will look something like this:
      <img width="1284" alt="Screenshot 2022-11-09 at 12 29 34 PM" src="https://user-images.githubusercontent.com/66726759/200900819-6e9f94a3-e85e-4c86-bb1f-713a25e400fb.png">
   - To further add more featuers, we can place a button under the video which can pause and play the video.
   - For this we need to create a ```vide_player.js``` javascript file in the ```video``` folder.
   - For our landing page to recognize the javascript file, we need to add the below ```<script>``` tag in our ```landing_page.html``` file.
        ```
        <script src="../video/video_player.js"></script>
        ```
   - The code for the ```play/pause``` functionality is: 
        ```
        var myVideo = document.getElementById("video1"); 

        function playPause() { 
          if (myVideo.paused) 
            myVideo.play(); 
          else 
            myVideo.pause(); 
        } 

        ```
        💡 When the ```play/pause``` button is clicked in the landing page, then the ```playPause()``` function is called. The video element is saved in            the variable ```myVideo```. Then inside the ```playPause()``` function an if condition is executed to check if the video is paused or played.
   
   - Finally, after the above modifications our page will look like this:

        
![Screenshot 2022-11-09 at 11 44 27 PM](https://user-images.githubusercontent.com/66726759/200902495-89dd025c-e2fd-44a4-9502-e6108e4e7b31.png)
        



