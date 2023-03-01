<!DOCTYPE html>
<html>
  <head>
    <title>Get User Geolocation</title>
  </head>
  <body>
    <button onclick="getLocation()">Get Location</button>
    <p id="demo"></p>
    <script>
      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(showPosition);
        } else {
          document.getElementById("demo").innerHTML = "Geolocation is not supported by this browser.";
        }
      }

      function showPosition(position) {
        document.getElementById("demo").innerHTML = "Latitude: " + position.coords.latitude +
        "<br>Longitude: " + position.coords.longitude;
      }
    </script>
  </body>
</html>
