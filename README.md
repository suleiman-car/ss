<!doctype html>
<html>
 <
 <body> 
  <script>
document.write('Number of Seat');

document.write("<input type='range' value='1' step='1' min='1' max='10' name='seat_slide' id='seat_slide'> <h4 id='seat_number'>0</h4> <p>₦<h4 id='total_fare'>30.00 </h4></p>");


var slider = document.getElementById("seat_slide");
  var seat_value = document.getElementById("seat_number");
  var fare_value = document.getElementById("total_fare"); 
  
  seat_value.innerHTML = slider.value; // Display the default slider value
  
  // Update the current slider value (each time you drag the slider handle)
  slider.oninput = function() {
    seat_value.innerHTML = this.value;
    
    var total = seat_value.innerHTML = this.value;
    document.getElementById("total_fare").innerHTML = (total * 30.00).toFixed(2);
    
  } 
</script> 
  <noscript>
    Number of Seat (₦30 per seat): 
   <input type="number" class="form-control" placeholder="1 to 10" min="1" max="10" required> 
  </noscript> 
 </body>
</html>
