
      
  
      <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animal Image Slider</title>
  <style>
    /* Style for the image slider container */
    .slider-container {
      position: relative;
      max-width: 100%;
      margin: auto;
      overflow: hidden;
    }

    /* Style for the images */
    .slide {
      display: none;
      width: 100%;
      height: auto;
      text-align: center;
    }

    .slide img {
      width: 100%;
      height: auto;
      border-radius: 10px;
    }

    /* Style for the animal name */
    .animal-name {
      position: absolute;
      bottom: 10px;
      left: 0;
      width: 100%;
      text-align: center;
      color: white;
      font-size: 18px;
      background-color: rgba(0, 0, 0, 0.5);
      padding: 5px;
    }
    
    /* Style for the animal image */
    .animal-image {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      margin-right: 5px;
      vertical-align: middle;
    }

    /* Style for the navigation arrows */
    .prev, .next {
      cursor: pointer;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: auto;
      padding: 16px;
      margin-top: -22px;
      color: white;
      font-weight: bold;
      font-size: 20px;
      background-color: rgba(0, 0, 0, 0.5);
      border-radius: 0 3px 3px 0;
    }

    .prev {
      left: 0;
      border-radius: 3px 0 0 3px;
    }

    .next {
      right: 0;
      border-radius: 0 3px 3px 0;
    }
  </style>
</head>
<body>

<div class="slider-container">
  <!-- Images -->
  <div class="slide">
    <img src="https://via.placeholder.com/800x400?text=Rabbit" alt="Rabbit">
    <div class="animal-name"><img class="animal-image" src="https://via.placeholder.com/50x50?text=Rabbit" alt="Rabbit"> Rabbit</div>
  </div>
  <div class="slide">
    <img src="https://via.placeholder.com/800x400?text=Tiger" alt="Tiger">
    <div class="animal-name"><img class="animal-image" src="https://via.placeholder.com/50x50?text=Tiger" alt="Tiger"> Tiger</div>
  </div>
  <div class="slide">
    <img src="https://via.placeholder.com/800x400?text=Dog" alt="Dog">
    <div class="animal-name"><img class="animal-image" src="https://via.placeholder.com/50x50?text=Dog" alt="Dog"> Dog</div>
  </div>
  <div class="slide">
    <img src="https://via.placeholder.com/800x400?text=Raccoon" alt="Raccoon">
    <div class="animal-name"><img class="animal-image" src="https://via.placeholder.com/50x50?text=Raccoon" alt="Raccoon"> Raccoon</div>
  </div>

  <!-- Navigation arrows -->
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>

<script>
  let slideIndex = 1;
  showSlides(slideIndex);

  function plusSlides(n) {
    showSlides(slideIndex += n);
  }

  function currentSlide(n) {
    showSlides(slideIndex = n);
  }

  function showSlides(n) {
    let i;
    const slides = document.getElementsByClassName("slide");
    if (n > slides.length) {slideIndex = 1}    
    if (n < 1) {slideIndex = slides.length}
    for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";  
    }
    slides[slideIndex-1].style.display = "block";  
  }
</script>

</body>
</html>


    
