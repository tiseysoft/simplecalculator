<!doctype HTML>
<html lang="en">
<head.
<meta charset="utf-8">
<title>simple caculator</title>
<link href="https://fonts.googleapis.com/css?family=Indie+Flower" rel="stylesheet">
<style>
   * {
   	font-family: 'Indie Flower', cursive;
   	color: #555;
   }
   body{
     background-color: #3fb399;
   }
   .container {
   	   width: 320px;
   	   background-color: white;
   	   margin: 120px auto;
   }
   table{
   	  width: 100%;
   	  border-color: #f4f4f4;
   }
   td{
   	width: 25%;
   }
   button{
   	width: 100%;
   	height: 70px;
   	font-size: 24px;
   	background-color: white;
   	border: none;
   }
   #inputlabel: {
   	  height: 120px;
   	  font-size: 40px;
      vertical-align: bottom;
      text-align: right;
      padding-right: 16px;
      background-color: #ececec;

   }
</style>
</head>
<body>
<div class="container">
  <table border="1" cellspacing="0">
     <tr>
         <td colspan="4" id="inputlabel">0</td>
     </tr>
     <tr>
        <td colspan="3"><button onclick="pushBtn(this);">AC</button></td>
        <td><button onclick="pushBtn(this);">/</button></td>
     </tr>
     <tr>
         <td><button onclick="pushBtn(this);">7</button></td>
         <td><button onclick="pushBtn(this);">8</button></td>
         <td><button onclick="pushBtn(this);">9</button></td>
         <td><button onclick="pushBtn(this);">*</button></td>
     </tr>
     <tr>
         <td><button onclick="pushBtn(this);">4</button></td>
         <td><button onclick="pushBtn(this);">5</button></td>
         <td><button onclick="pushBtn(this);">6</button></td>
         <td><button onclick="pushBtn(this);">-</button></td>
     </tr><tr>
         <td><button onclick="pushBtn(this);">1</button></td>
         <td><button onclick="pushBtn(this);">2</button></td>
         <td><button onclick="pushBtn(this);">3</button></td>
         <td><button onclick="pushBtn(this);">+</button></td>
     </tr>
     <tr>
         <td colspan="2"><button onclick="pushBtn(this);">0</button></td>
         <td><button onclick="pushBtn(this);">.</button></td>
         <td><button onclick="pushBtn(this);">=</button></td>
     </tr>
  </table>
</div>
<script>
    var inputlabel = document.getElementById('inputLabel');
    function pushBtn(obj) {
      var pushed = obj.innerHTML;
      if (pushed == "=") {
          //calculete
          inputLabel.innerHTML = eval(inputLabel.innerHTML);
      }else if (pushed == 'AC') {
        //All Clear
        inputLabel.innerHTML = '0';

      } else {
        if (innerLabel.innerHTML == '0'){
            inputLabel.innerHTML = pushed;


        } else{
          inputLabel.innerHTML += pushed;
        }
      }
    }

</script>
</body>
</html>
