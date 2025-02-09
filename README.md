<!--
Lyna Pham
patient-form.html
09/07/2024
09/21/2024
Version: 3.2
Description: a page that has a form on it to register a new account and capture demographic data.
-->


<!DOCTYPE html>
<html lang="en-US">
<link rel="stylesheet" href="styles.css"
<body>
<h1> <img src="Caduceus.jpg"
style=width:70px; height:70px;> Lyna's Clinic
</h1>


  <!-- Date element -->


  <p style="text-align: center;" id="date"></p>



  <script>
    /* First two arrays are to convert the int values returned by the JS date object functions into strings */


    const daysOfWeek = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday']
    const monthsOfYear = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']


    /* Today's date veriables */


    let rawDate = new Date()
    let day = daysOfWeek[rawDate.getDay()]
    let month = monthsOfYear[rawDate.getMonth()]
    let date = rawDate.getDate()
    let year = rawDate.getFullYear()



    let date2 = null


    if (date > 3 && date < 21) {
      date2 = date.toString() + 'th'
    } else {
      switch (date % 10) {
        case 1:
          date2 = date.toString() + 'st'
          break
        case 2:
          date2 = date.toString() + 'nd'
          break
        case 3:
          date2 = date.toString() + 'rd'
          break
        default:
          date2 = date.toString() + 'th'
          break
      }
    }


    /* This code grabs the header date HTML element and places the final date string inside it */


    document.getElementById("date").innerHTML = "Today is: " + day + ", " + month + " " + date2 + ", " + year + "."


  </script>


<!-- Registration form begins -->
<h3> Patient Registration Form </h3>


    <!-- Name -->


<center>
<table style="text-align: center">
  <tr>
    <td>
      <form action="homework1-thankyou.html">
      <label for="fname"> First Name: </label>
      <input type="text" maxlength="30" id="fname" name="fname" placeholder="Enter your first name" required>
    </td>
&nbsp;
    <td>
      <label for="minitial"> Middle Initial:</label>
      <input type="text" maxlength="1" size="1" id="minitial" name="minitial">
    </td>
&nbsp;
    <td>
      <label for="lname"> Last Name:</label>
      <input type="text"  maxlength="30" id="lname" name="lname" placeholder="Enter your last name" required>
    </td>


  <br> <br>
  </tr>


<!-- Date of Birth, Age, Social Security Number  -->
  <tr>
      <td>
  <label for="birthday"> Date of Birth:</label>
  <input type="text" pattern="[0-9]{2}/[0-9]{2}/[0-9]{4}" id="bday" name="bday" placeholder="MM/DD/YYYY" required>
      </td>
  &nbsp;
      <td>
  <label for="age"> Age:</label>
  <input tpye="text"  maxlength="3" size="2" id="age" name="age" required>
      </td>
  &nbsp
      <td>
  <label for="ssn"> Social Security Number:</label>
  <input tpye="text"  minlength="9" maxlength="11" size="14" id="ssn" name="ssn" placeholder="Enter your SSN" required>
      </td>
    </tr>
 
 
  <br> <br>


<!-- Gender -->


  <tr>
    <td></td>
    <td>
  <label for="sex"> Sex:</label> <br>
  <input type="radio" id="male" name="gender" value="Male">
  <label for="gender"> Male </label>


  <input type="radio" id="female" name="gender" value="Female">
  <label for="gender"> Female </label>
&nbsp;
  <input type="radio" id="other" name="gender" value="Other">
  <label for="gender"> Other</label>
  <input type="text" size="12" id="other" name"other" placeholder="if other, specify">
    </td>
    <td></td>
  </tr>
</table>
<!-- Address  -->


<br>
<center>
<table>
  <tr>
    <td>
  <label for="address1"> Address Line 1: </label>
  <input type="text" maxlength="30" size="60" id="address1" name="address1" placeholder="Enter your main address" required>
    </td>
  </tr>


  <tr>
    <td>
  <label for="address2"> Address Line 2: </label>
  <input type="text" maxlength="30" size="60" id="address2" name="address2" placeholder="Enter your secondary address or N/A">
    </td>
  </tr>


 </table>
  <br> <br>




<!-- City -->
<center>
<table>
  <tr>
    <td>
  <label for="city"> City:</label>
  <input type="text"  maxlength="30" id="city" name="city" placeholder="Enter your city"required>
  &nbsp;
  </td>
 
<!-- States/DC/PR -->


  <td>


  <label for="state">State:</label>
 <select name="state" id="state">
 <option disabled selected value> -- select an option -- </option>
 <option value="AL">Alabama</option>
 <option value="AK">Alaska</option>
 <option value="AZ">Arizona</option>
 <option value="AR">Arkansas</option>
 <option value="CA">California</option>
 <option value="CO">Colorado</option>
 <option value="CT">Connecticut</option>
 <option value="DE">Delaware</option>
 <option value="DC">District Of Columbia</option>
 <option value="FL">Florida</option>
 <option value="GA">Georgia</option>
 <option value="HI">Hawaii</option>
 <option value="ID">Idaho</option>
 <option value="IL">Illinois</option>
 <option value="IN">Indiana</option>
 <option value="IA">Iowa</option>
 <option value="KS">Kansas</option>
 <option value="KY">Kentucky</option>
 <option value="LA">Louisiana</option>
 <option value="ME">Maine</option>
 <option value="MD">Maryland</option>
 <option value="MA">Massachusetts</option>
 <option value="MI">Michigan</option>
 <option value="MN">Minnesota</option>
 <option value="MS">Mississippi</option>
 <option value="MO">Missouri</option>
 <option value="MT">Montana</option>
 <option value="NE">Nebraska</option>
 <option value="NV">Nevada</option>
 <option value="NH">New Hampshire</option>
 <option value="NJ">New Jersey</option>
 <option value="NM">New Mexico</option>
 <option value="NY">New York</option>
 <option value="NC">North Carolina</option>
 <option value="ND">North Dakota</option>
 <option value="OH">Ohio</option>
 <option value="OK">Oklahoma</option>
 <option value="OR">Oregon</option>
 <option value="PA">Pennsylvania</option>
 <option value="PR">Puerto Rico</option>
 <option value="RI">Rhode Island</option>
 <option value="SC">South Carolina</option>
 <option value="SD">South Dakota</option>
 <option value="TN">Tennessee</option>
 <option value="TX">Texas</option>
 <option value="UT">Utah</option>
 <option value="VT">Vermont</option>
 <option value="VA">Virginia</option>
 <option value="WA">Washington</option>
 <option value="WV">West Virginia</option>
 <option value="WI">Wisconsin</option>
 <option value="WY">Wyoming</option>
 </select>


  </td>
<!-- Zipcode -->
    <td>
  &nbsp;
  <label for="zipcode"> Zipcode:</label>
  <input type="text"  minlength="5" maxlength="10" size="16" id="zipcode" name="zipcode" placeholder="Enter your zipcode" required>
    </td>


</tr>
</table>


<br>
<!-- Email&Phone -->


<center>
<table>
  <tr>
    <td>
  <label for="email"> Email Address:</label>
  <input type="text" id="email" name="email" size="22" placeholder="Enter your Email Address"required>
    </td>
    <td>
  <label for="phone"> Phone Number:</label>
  <input type="phone" id="phone" name="phone" maxlength= "12" placeholder="123-456-7890"
 pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" required>
    </td>
  </tr>
</table>
<br>
<!-- Slider  -->


<center>
<table>
  <tr>
    <td>
 <div class="slidecontainer">
  <label for="painscale"> Pain Scale: </label>
  <input style="accent-color: rgb(0,200,400) " type="range" min="1" max="10" value="1">
    </td>
  </tr>


<!-- Symptoms Box -->
  <tr>
    <td>
<label for="Symptoms"> Additional Information/Current Symptoms: </label>
    </td>
  </tr>
  <tr>
    <td>
 <textarea name="Symptoms" rows="10" cols="50"> </textarea>
    </td>
  </tr>
</table>


<!-- Medical History -->
<center>
<table>
  <tr>
   <td>
  <label for="MedicalHistory"> Medical History: </label>
   </td>
  </tr>


  <tr>
    <td>
  <input type="checkbox" id="cpox" name="cpox" value="Chicken Pox">
  <label for="cpox"> Chicken Pox</label>
    </td>
    <td>
  <input type="checkbox" id="measles" name="measles" value="Measles">
  <label for="Measles"> Measles</label>
    </td>
    <td>
  <input type="checkbox" id="covid" name="covid" value="Covid-19">
  <label for="covid"> Covid-19</label>
    </td>
    <td>
  <input type="checkbox" id="spox" name="spox" value="Small Pox">
  <label for="spox"> Small Pox</label>
    </td>
    <td>
  <input type="checkbox" id="tnusu" name="tnus" value="Tetanus">
  <label for="tnus"> Tetanus</label>
    </td>
  </tr>
</table>
<!-- Registration (User&P) -->


<br> <br>
<center>
<table>
  <tr>
    <td>
  <label for="username">Username:</label>
  <input type="text" maxlength="20" id="username" name="username" placeholder="Create a username" required> <br>
    </td>
  </tr>


  <tr>
    <td>
  <label for="pwd">Password:</label>
  <input type="password" id="pwd" name="pwd" placeholder="Create a password" required> <br>
    </td>
  </tr>


  <tr>
    <td>
  <label for="againpwd"> Re-Enter Password:</label>
  <input type="password" id="againpwd" name="againpwd" placeholder="Re-enter your password"required>
    </td>
  </tr>
  </table>


<!-- Reset & Submit -->


<br> <br>
<input type="reset" value="Reset">
&nbsp;
<input type="submit" value="Submit">
</form>


</body>


<!-- Footer -->


<footer>
<p>Lyna's Clinic
&nbsp;
<a href="https://docs.google.com/document/d/1dA4PvSyoWyjeQkJBrCoPxw11v3Cvc__PSlO6LMi_Tak/edit?usp=sharing">Contact Us!</a>
</p>
<p>PO BOX 70248</p>
<p>Houston TX, 77083</p>
</footer>


</html>
