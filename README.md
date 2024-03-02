# ip-ex-5
<!DOCTYPE html>
<html>
<head>
<script>
function validateForm() {
  let name = document.forms["myForm"]["fname"].value;
  let age = document.forms["myForm"]["age"].value;
  let birthdate = document.forms["myForm"]["birthdate"].value;
  let email = document.forms["myForm"]["email"].value;
  let continent = document.forms["myForm"]["continent"].value;
  let cool = document.querySelector('input[name="cool"]:checked');
  let colors = document.querySelectorAll('input[name="colors"]:checked');
  let frameworks = document.querySelectorAll('input[name="framework"]:checked');

  if (name == "") {
    alert("Name must be filled out");
    return false;
  }
  if (age == "") {
    alert("Age must be filled out");
    return false;
  }
  if (birthdate == "") {
    alert("Birthdate must be filled out");
    return false;
  }
  if (email == "") {
    alert("Email is required");
    return false;
  }
  if (continent == "") {
    alert("Continent must be filled out");
    return false;
  }
  if (!cool) {
    alert("Please answer 'Are you cool?'");
    return false;
  }
  if (colors.length !== 2) {
    alert("Please select exactly 2 colors");
    return false;
  }
  if (frameworks.length === 0) {
    alert("Please select at least one framework");
    return false;
  }
}
</script>
</head>
<body>

<h2>JavaScript Validation</h2>

<form name="myForm" action="/action_page.php" onsubmit="return validateForm()" method="post">
  Name: <input type="text" name="fname"><br><br>
  Age: <input type="text" name="age"><br><br>
  Birthdate: <input type="text" name="birthdate"><br><br>
  Email: <input type="text" name="email"><br><br>
  Continent:
  <select name="continent">
    <option value="">Select Continent</option>
    <option value="Africa">Africa</option>
    <option value="Asia">Asia</option>
    <option value="Europe">Europe</option>
    <option value="North America">North America</option>
    <option value="South America">South America</option>
    <option value="Australia">Australia</option>
    <option value="Antarctica">Antarctica</option>
  </select><br><br>
  Are you cool?
  <input type="radio" name="cool" value="yes"> Yes
  <input type="radio" name="cool" value="no"> No<br><br>
  What 2 colors do you like?<br>
  <input type="checkbox" name="colors" value="red"> Red<br>
  <input type="checkbox" name="colors" value="blue"> Blue<br>
  <input type="checkbox" name="colors" value="green"> Green<br>
  <input type="checkbox" name="colors" value="yellow"> Yellow<br><br>
  What do you like?<br>
  <input type="checkbox" name="framework" value="codeigniter"> CodeIgniter<br>
  <input type="checkbox" name="framework" value="fuel"> Fuel<br>
  <input type="checkbox" name="framework" value="kohana"> Kohana<br>
  <input type="checkbox" name="framework" value="laravel"> Laravel<br>
  <input type="checkbox" name="framework" value="zend"> Zend<br><br>
  <input type="submit" value="Submit">
</form>

</body>
</html>
