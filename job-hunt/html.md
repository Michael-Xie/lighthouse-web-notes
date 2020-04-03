# HTML

## textContent vs innerHTML
- textContext sets and gets text from element
- innerHTML gets and sets html from element

## Get geolocation from user
if (navigator.geolocation){
  navigator.geolocation.getCurrentPosition(function(position) {
    document.getElementById('data').innerHTML="latitude: " + position.coords.latitude + "<br>longitude: " + position.coords.longitude;
  });
}
