# practiceApp

<!DOCTYPE html>
<html>

<head>
    <title>PracticeApp</title> 
    <link rel="stylesheet" href="style.css"> 
    <meta charset="utf-8">  
</head>
  
  
<body>
<h1 align="center">Maitre D </h1>
<br>
<div>
    <table align="center">
<form id="practiceapp" name="practiceapp">
<tr>
<td>
  <label for="iPrice">iPrice:</label>
  <input type="Number" id="iPrice" value="00.00" step="1.00">
</td>
</tr>
<td> 

  <label for="tips">tips   :</label>
  <input type="Number" id="tips" value="00.00" step="1.00">
</td>

  <label class="total">Total</label>
  <input type="text" id="Total" readonly>
  <input type="submit" value="calculate"/>
</form>

</table>
</div>

<script>
var calculateTotal = function(price) {
  price.preventDefault();
  var iprice = parseInt(document.getElementById("iPrice").value);
  var Tips = parseInt(document.getElementById("tips").value);
  var tax = .055;
  var total = Tips + (iprice * tax) + iprice
  document.getElementById("Total").value = total;
  
}
var form = document.getElementById('practiceapp');
form.addEventListener('submit', calculateTotal, false);
</script>
</body>
</html>
