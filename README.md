# JeNetwork.github.io
Tool for render video by FFmpeg
<textarea id="tbx1" style="width:380px; height:80px; font-size:16pt;">33,34,38,40,46,49,51,57,59,63,64,68,72,74,78,87,86,89,90,94,98</textarea>
<input type="button" value="Click Me!" onclick="Loto();" style="width:100px; height:40px; font-size:14pt;"/><br/>
<b id="lb1" style="font-size:16pt; color:green;"></b><br/>
<b id="lb2" style="font-size:16pt; color:green;"></b><br/>
<b id="lb6" style="font-size:16pt; color:green;"></b><br/>
<b id="lb3" style="font-size:16pt; color:red;"></b><br/>
<b id="lb4" style="font-size:16pt; color:red;"></b><br/>
<b id="lb5" style="font-size:16pt; color:red;"></b><br/>
<textarea id="tbx2" style="width:380px; height:500px;"></textarea>

<script language="JavaScript" type="text/javascript">
function Loto()
{
  var string = document.getElementById("tbx1").value;
  //var array = string.split(',').map(function(n) {return Number(n);});
  var array = string.split(',');
  var sb="";
  for(let i=0; i<array.length; i++) {	sb+="0"+array[i]+",1"+array[i]+",2"+array[i]+",3"+array[i]+",4"+array[i]+",5"+array[i]+",6"+array[i]+",7"+array[i]+",8"+array[i]+",9"+array[i]+","; }
  var n1 = array.length * 230; var n1s=n1.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  var n2 = array.length * 170; var n2s=n2.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  var d3=3*n2; var d4=4*n2; var d5=5*n2; var d6=6*n2;
  document.getElementById("tbx2").value = sb;
  document.getElementById("lb1").innerHTML = array.length + " x 230 = " + n1s;
  document.getElementById("lb2").innerHTML = array.length + " x 170 = " + n2s;
  document.getElementById("lb6").innerHTML = n2s + " x 3 = " + d3.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K + " + n1s + " = " + (n1+d3).toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  document.getElementById("lb3").innerHTML = n2s + " x 4 = " + d4.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K + " + n1s + " = " + (n1+d4).toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  document.getElementById("lb4").innerHTML = n2s + " x 5 = " + d5.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K + " + n1s + " = " + (n1+d5).toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  document.getElementById("lb5").innerHTML = n2s + " x 6 = " + d6.toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K + " + n1s + " = " + (n1+d6).toString().replace(/\B(?=(\d{3})+\b)/g, ",") + "K";
  navigator.clipboard.writeText(sb); // Copy to Clipboard
}
</script>
