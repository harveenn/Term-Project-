<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
 <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat">
 <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>
     ul{
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 10%;
        background-color: #957;
        position: fixed;
        height: 100%;
        overflow: auto;
    }
    li a {
        display: block;
        color: white;
        padding: 8px 16px;
        text-decoration: none;
        text-align: center;
    }
    li a.active {
        color: white;
    }
    li a:hover:not(.active) {
        background-color: #957DAD;
        color: white;
    }
    h1{
        color: white;
        text-align: center;
    }
    /* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}
 .prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -22px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}
.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.8);
}
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}
.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}
.active, .dot:hover {
  background-color: #717171;
}
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}
@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}
</style>

  <ul>
   <br><br><br><br><br><br>
    <li>
        <a href="home.html">
            <i class="fa fa-home w3-xxlarge"></i>
            <p>HOME</p>
        </a>
    </li>
    <li>
        <a href="aboutme.html">
            <i class="fa fa-user w3-xxlarge"></i>
            <p>ABOUT</p>
          </a>
    </li>
    <li>
        <a href="photos.html">
            <i class="fa fa-eye w3-xxlarge"></i>
            <p>PROJECTS</p>
          </a>
    </li>
    <li> <a href="contact.html">
        <i class="fa fa-envelope w3-xxlarge"></i>
        <p>CONTACT</p>
    </li>
  </ul>
<body>
<h1>Harveen's Portfolio</h1>

<div class="slideshow-container">
    <div class="mySlides fade">
      <div class="numbertext">1 / 3</div>
      <img src="img_nature_wide.jpg" style="width:100%">
      <div class="text">Caption Text</div>
    </div>
    <div class="mySlides fade">
      <div class="numbertext">2 / 3</div>
      <img src="img_snow_wide.jpg" style="width:100%">
      <div class="text">Caption Two</div>
    </div>
    <div class="mySlides fade">
      <div class="numbertext">3 / 3</div>
      <img src="img_mountains_wide.jpg" style="width:100%">
      <div class="text">Caption Three</div>
    </div>
    <a class="prev" onclick="plusSlides(-1)">❮</a>
    <a class="next" onclick="plusSlides(1)">❯</a>
    </div>
    <br>
    <div style="text-align:center">
      <span class="dot" onclick="currentSlide(1)"></span> 
      <span class="dot" onclick="currentSlide(2)"></span> 
      <span class="dot" onclick="currentSlide(3)"></span> 
    </div>

</body>
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
      let slides = document.getElementsByClassName("mySlides");
      let dots = document.getElementsByClassName("dot");
      if (n > slides.length) {slideIndex = 1}    
      if (n < 1) {slideIndex = slides.length}
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";  
      }
      for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
      }
      slides[slideIndex-1].style.display = "block";  
      dots[slideIndex-1].className += " active";
    }
    </script>
</html>
