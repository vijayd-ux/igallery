# Ex.08 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

```
HTML CODE:   
   
    <html>
<head>
    <title>Image Gallery</title>
    <link rel="stylesheet" href="bb.css">
    <script src="script.js"></script>
</head>
<body>

    <div class="head">DBL Image Gallery</div>

    <div class="main-content">
        <div class="gallery-container">
            <img id="galleryImage" class="gallery-image" src="BEAST GOHAN.jpg">
            <div id="caption" class="caption"></div>
            <div class="gallery-buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <div class="footer-banner">
        VIJAY D(25015213)
    </div>
</body>
</html>

CSS CODE:

body {
    display: flex;
    flex-direction: column;
    height: 100vh;

    background: bisque
}

.head {
    background-color: rgb(225, 225, 121);
    color: rgb(18, 74, 88);
    text-align: center;
    padding: 15px;
    font-size: 42px;
    font-weight: bold;
    text-shadow: 3px 3px 0px bisque;
}

.main-content {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.gallery-container {
    background: rgb(18, 74, 88);
    padding: 25px;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 700px;
    border: 8px solid black;
}

.gallery-image {
    width: 700px;
    height: 1000px;
    object-fit: cover;
    border-radius: 10px;
    border: 3px solid black;
}

.caption {
    margin: 20px;
    font-size: 18px;
    font-weight: 500;
}

.gallery-buttons {
    display: flex;
    justify-content: center;
    gap: 10px;
}

button {
    padding: 10px 25px;
    cursor: pointer;
    border: none;
    border-radius: 7px;
    background-color: blanchedalmond;
    color: rgb(36, 50, 40);
    font-size: 18px;
    transition: background 0.4s;
}

button:hover {
    background-color: rgb(232, 198, 157);
}

.footer-banner {
    background-color: rgb(101, 155, 132);
    color: whitesmoke;
    text-align: center;
    padding: 10px;
    font-size: 24px;
    font-weight: 100px;
}

JAVA CODE:

const gallery = [
    { src: "BEAST GOHAN.jpg", caption: "BEAST GOHAN" },
    { src: "gogeta blue.webp", caption: "SSJ GOGETA BLUE" },
    { src: "MUI GOKU.webp", caption: "MUI GOKU" },
    { src: "GOKU BLACK.png", caption: "GOKU BLACK" },
    { src: "SSJ4 GOGETA.webp",caption:"SSJ4 GOGETA"},
    { src: "UI GOKU 2.jpg",caption:"UI GOKU -sign-"},
];

let index = 0;

function updateGallery() {
    document.getElementById("galleryImage").src = gallery[index].src;
    document.getElementById("caption").textContent = gallery[index].caption;
}

function nextImage() {
    index++;
    if (index >= gallery.length) {
        index = 0;
    }
    updateGallery();
}

function prevImage() {
    index--;
    if (index < 0) {
        index = gallery.length - 1;
    }
    updateGallery();
}
```

## OUTPUT:
![alt text](<Screenshot 2025-12-27 110317-1.png>) 
![alt text](<Screenshot 2025-12-27 110348-1.png>) 
![alt text](<Screenshot 2025-12-27 110409-1.png>) 
![alt text](<Screenshot 2025-12-27 110422-1.png>) 
![alt text](<Screenshot 2025-12-27 110438-1.png>) 
![alt text](<Screenshot 2025-12-27 110459-1.png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
