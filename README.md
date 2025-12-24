# Ex.08 Design of Interactive Image Gallery
## Date:19/12/25
## REF NO:25007890
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
~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MY GALLERY</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #e8eeef;
    }

    .gallery-container {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      padding: 20px;
      justify-content: center;
    }

    .gallery-item {
      width: 200px;
      height: 150px;
      overflow: hidden;
      cursor: pointer;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(12, 215, 93, 0.1);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    .lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    .lightbox-image {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(223, 123, 8, 0.252);
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: #fff;
      cursor: pointer;
      z-index: 1001;
    }

    .close:hover {
      color: #ff6b6b;
    }
    .footer {
        text-align: center;
        margin-top:40%;
        background-color: bisque;
        color:black;
        font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        font-size: 30px;
    }
  </style>
</head>
<body>
    <center>
  <div class="gallery-container">
    <div class="gallery-item">
      <img src=https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQOT1GqVev_dSFVOVwlnYh8p5yh6t7230Jzcg&s alt="Image 1">
    </div>
    <br>
    <div class="gallery-item">
      <img src="https://i.pinimg.com/736x/4a/39/de/4a39de35931e5ca4901b4fda3f43e71c.jpg" alt="Image 2">
    </div>
    <br>
    <div class="gallery-item">
      <img src="https://images.stockcake.com/public/5/f/9/5f9c2b86-0649-41ea-b6ae-bb07385c78f5_large/sunset-over-ocean-stockcake.jpg" alt="Image 3">
    </div>
    <br>
    <div class="gallery-item">
        <img src="https://st2.depositphotos.com/2627021/6665/i/450/depositphotos_66650665-stock-photo-romantic-and-scenic-panorama-with.jpg" alt="Image 4">
    </div>
    <br>
    <div class="gallery-item">
        <img src=https://static.vecteezy.com/system/resources/previews/049/316/573/non_2x/lotus-flower-blue-photo.jpg alt="Image 5">
    </div>
    <br>
    <div class="gallery-item">
        <img src=https://media.istockphoto.com/id/1300970146/photo/impressive-summer-sunrise-on-eibsee-lake-with-zugspitze-mountain-range-sunny-outdoor-scene-in.jpg?s=612x612&w=0&k=20&c=qH7-_lkSaUJKWUI29rqR-eaXvZd_9-5_QEtjruqkFdk= alt="Image 6">
    </div>
</center>
    <br>
    </div>
  <div class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-image" src="" alt="Enlarged Image">
  </div>
 

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const galleryItems = document.querySelectorAll('.gallery-item img');
      const lightbox = document.querySelector('.lightbox');
      const lightboxImage = document.querySelector('.lightbox-image');
      const closeBtn = document.querySelector('.close');

      // Open lightbox on image click
      galleryItems.forEach(item => {
        item.addEventListener('click', () => {
          lightbox.style.display = 'flex';
          lightboxImage.src = item.src;
        });
      });

      // Close lightbox on close button click
      closeBtn.addEventListener('click', () => {
        lightbox.style.display = 'none';
        lightboxImage.src = '';
      });

      // Close lightbox on clicking outside the image
      lightbox.addEventListener('click', (e) => {
        if (e.target !== lightboxImage) {
          lightbox.style.display = 'none';
          lightboxImage.src = '';
        }
      });
    });
  </script>
</body>
</html>
~~~
## OUTPUT:
<img width="904" height="976" alt="526176458-ae34de8e-ae3a-45fc-8f13-c2a04ad449e5" src="https://github.com/user-attachments/assets/14355c2e-96fd-4c41-afd5-aad6e5aaac9c" />
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
