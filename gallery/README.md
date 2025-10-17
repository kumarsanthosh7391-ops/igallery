Date:17/10/2025
AIM:
To design a web application for an inteactive image gallery with minimum five images.

DESIGN STEPS:
Step 1:
Clone the github repository and create Django admin interface.

Step 2:
Change settings.py file to allow request from all hosts.

Step 3:
Use CSS for positioning and styling.

Step 4:
Write JavaScript program for implementing interactivity.

Step 5:
Validate the HTML and CSS code.

Step 6:
Publish the website in the given URL.

PROGRAM :
```
ll.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>santhosh kumar s-25017512</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="header-content">
            <h1>santhosh kumar s| IMAGE GALLERY</h1>
            <p class="subtitle">A Gallery of MEMORIES</p>
        </div>
    </header>

    <main class="gallery-container">
        
        <div class="image-grid">
            <div class="gallery-item">
                <img src="WhatsApp Image 2025-09-20 at 21.43.12_d14d05b2.jpg" alt="Image 1" data-caption="I am">
            </div>
            <div class="gallery-item">
                <img src="WhatsApp Image 2025-09-20 at 21.43.19_66007865.jpg" alt="Image 2" data-caption="Bro">
            </div>
            <div class="gallery-item">
                <img src="WhatsApp Image 2025-09-20 at 21.43.37_a1b46b17.jpg" alt="Image 3" data-caption="with my friends">
            </div>
            <div class="gallery-item">
                <img src="WhatsApp Image 2025-09-20 at 21.43.38_0c30aed8.jpg" alt="Image 4" data-caption=" with my roomate ">
            </div>
        </div>

        <div id="modal" class="modal">
            <span class="close" id="close">&times;</span>
            <img class="modal-content" id="modal-img">
            <div id="caption" class="modal-caption"></div>
        </div>
        
    </main>

    <footer class="footer">
        <p>&copy; 2025 Image Gallery | Developed by: <span class="designer-name">santhosh kumar s-25017512</span></p>
    </footer>

    <script src="java.js"></script>
</body>
</html>
style.css
body {
    font-family: 'Montserrat', sans-serif; 
    margin: 0;
    padding: 0;
    background-color: white; 
    display: flex;
    flex-direction: column; 
    align-items: center;
    min-height: 100vh; 
    overflow-x: hidden;
}
header {
    background-color: white; 
    color: blue;
    padding: 40px 20px;
    width: 100%;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    text-align: center;
}

header h1 {
    font-size: 2.2em;
    margin: 0;
    letter-spacing: 2px;
    border-bottom: 2px solid green; 
    display: inline-block;
    padding-bottom: 5px;
}

.subtitle {
    font-size: 1.1em;
    color: yellow;
    margin-top: 10px;
    font-weight: 400;
}
java.js
document.addEventListener('DOMContentLoaded', () => {
    const images = document.querySelectorAll('.gallery-item img');
    const modal = document.getElementById('modal');
    const modalImg = document.getElementById('modal-img');
    const closeBtn = document.getElementById('close');
    const captionText = document.getElementById('caption'); 

    images.forEach((image) => {
        image.addEventListener('click', () => {
            modal.style.display = 'flex'; 
            modalImg.src = image.src;
            captionText.innerHTML = image.getAttribute('data-caption') || image.alt;
        });
    });

    closeBtn.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (event) => {
        if (event.target === modal) {
            modal.style.display = 'none';
        }
    });
});



```

OUTPUT:

RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.