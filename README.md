# Ex.08 Design of Interactive Image Gallery
# Date:10/05/2025S
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Types of Dogs</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&family=Comic+Neue:wght@700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #dff0d8, #b2dfdb, #c8e6c9);
      color: #2e2e2e;
      background-size: 300% 300%;
      animation: backgroundShift 12s ease infinite;
    }

    @keyframes backgroundShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    h1 {
      text-align: center;
      font-size: 3rem;
      margin: 40px 0 20px;
      font-family: 'Comic Neue', cursive;
      background: linear-gradient(to right, #4caf50, #81c784);
      -webkit-background-clip: text;
      color: transparent;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      padding: 30px;
      max-width: 1400px;
      margin: auto;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 16px;
      cursor: pointer;
      box-shadow: 0 10px 25px rgba(76, 175, 80, 0.3);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .gallery-item:hover {
      transform: scale(1.05);
      box-shadow: 0 20px 40px rgba(76, 175, 80, 0.5);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.15);
    }

    .caption {
      position: absolute;
      bottom: 0;
      background: rgba(255, 255, 255, 0.85);
      width: 100%;
      padding: 12px;
      text-align: center;
      font-size: 16px;
      color: #388e3c;
      font-weight: bold;
      letter-spacing: 1px;
    }

    .modal {
      display: none;
      position: fixed;
      inset: 0;
      background-color: rgba(0, 0, 0, 0.9);
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border: 5px solid #4caf50;
      border-radius: 12px;
      box-shadow: 0 0 40px #4caf50;
    }

    .modal .close {
      position: absolute;
      top: 25px;
      right: 35px;
      font-size: 40px;
      color: #fff;
      cursor: pointer;
      text-shadow: 0 0 15px #4caf50;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 18px;
      font-family: 'Comic Neue', cursive;
      color: #fff;
      background-color: #388e3c;
      border-top: 4px solid #a5d6a7;
    }
  </style>
</head>
<body>

  <h1>🐶 Types of Dogs</h1>

  <div class="gallery">
    <div class="gallery-item" onclick="openModal('lb.jpg')">
      <img src="lb.jpg" alt="Labrador Retriever">
      <div class="caption">Labrador Retriever</div>
    </div>
    <div class="gallery-item" onclick="openModal('gs.avif')">
      <img src="gs.avif" alt="German Shepherd">
      <div class="caption">German Shepherd</div>
    </div>
    <div class="gallery-item" onclick="openModal('be.jpg')">
      <img src="be.jpg" alt="Beagle">
      <div class="caption">Beagle</div>
    </div>
    <div class="gallery-item" onclick="openModal('pp.jpg')">
      <img src="pp.jpg" alt="Pomeranian">
      <div class="caption">Pomeranian</div>
    </div>
    <div class="gallery-item" onclick="openModal('poo.jpg')">
      <img src="poo.jpg" alt="Poodle">
      <div class="caption">Poodle</div>
    </div>
    <div class="gallery-item" onclick="openModal('hu.webp')">
      <img src="hu.webp" alt="Husky">
      <div class="caption">Husky</div>
    </div>
    <div class="gallery-item" onclick="openModal('dd.webp')">
      <img src="dd.webp" alt="Dachshund">
      <div class="caption">Dachshund</div>
    </div>
    <div class="gallery-item" onclick="openModal('shi.avif')">
      <img src="shi.avif" alt="Shiba Inu">
      <div class="caption">Shiba Inu</div>
    </div>
    <div class="gallery-item" onclick="openModal('grdd.jpg')">
      <img src="grdd.jpg" alt="Golden Retriever">
      <div class="caption">Golden Retriever</div>
    </div>
  </div>

  <!-- Modal -->
  <div class="modal" id="imageModal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="" alt="Dog Breed">
  </div>

  <footer>
    &copy; 2025 designed by BARKAVI (24901000). All Rights Reserved.
  </footer>

  <script>
    function openModal(src) {
      const modal = document.getElementById('imageModal');
      const modalImg = document.getElementById('modalImage');
      modalImg.src = src;
      modal.style.display = 'flex';
    }

    function closeModal() {
      const modal = document.getElementById('imageModal');
      modal.style.display = 'none';
    }
  </script>
</body>
</html>

```
# OUTPUT:
![alt text](<Screenshot 2025-05-11 014410.png>)

![alt text](<Screenshot 2025-05-11 014422.png>)

![alt text](<Screenshot 2025-05-11 014434.png>)

![alt text](<Screenshot 2025-05-11 014445.png>)

![alt text](<Screenshot 2025-05-11 014459.png>)

![alt text](<Screenshot 2025-05-11 014509.png>)

![alt text](<Screenshot 2025-05-11 014522.png>)

![alt text](<Screenshot 2025-05-11 014538.png>)

![alt text](<Screenshot 2025-05-11 014553.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
