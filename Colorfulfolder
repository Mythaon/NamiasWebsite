/*Slideshow*/
function _(x) {
  return document.getElementById(x);
}

var slideArray;
var slideIndex = 0;
var interval;
var slideContentArray = [
  '<h1>This Template Is Awesome!</h1><img src="img/laptop.svg" style="width:auto;max-height:480px;" alt="Picture of laptop">',
  '<h1>This Template Is Awesome!</h1><img src="img/computer-tablet-mobile.svg" style="width:auto;max-height:480px;" alt="Picture of computer, desktop, mobile">',
  '<h1>This Template Is Awesome!</h1><img src="img/desktop-computer.svg" style="width:auto;max-height:480px;" alt="Picture of desktop computer">'
];

function currentSlide(slideIndex) {
  _("slides").style.opacity = 0;

  for(var i = 0; i < slideArray.length; i++) {
    slideArray[i].style.background = "none";
  }

  slideArray[slideIndex].style.background = "#fff";

  setTimeout(function() {
    _("slides").innerHTML = slideContentArray[slideIndex];
    _("slides").style.opacity = 1;
  }, 500);
}

function slideshowSlide() {
  slideIndex++;

  if(slideIndex == slideArray.length) {
    slideIndex = 0;
  }

  currentSlide(slideIndex);
}

window.addEventListener("load", function() {
  slideArray = _("slideshow-buttons").children;
  interval = setInterval(slideshowSlide, 5000);
});

/*Zoom image*/
var modal = document.getElementById("myModal");
var img = document.getElementById("myImg");
var modalImg = document.getElementById("modal-image");

window.openModal = function(img){
    modal.style.display = "block";
    modalImg.src = img.getAttribute("src");
}

var span = document.getElementsByClassName("close")[0];

span.onclick = function() { 
    modal.style.display = "none";
};

window.onclick = function() {
  if(event.target == modal) {
    modal.style.display = "none";
  }
}

/*Page navigation scroll*/
$(document).ready(function(){
  $("a").on('click', function(event) {
    if (this.hash !== "") {
      event.preventDefault();
      var hash = this.hash;

      $('html, body').animate({
        scrollTop: $(hash).offset().top
      }, 900, function(){
           window.location.hash = hash;
      });
    }
  });
});
