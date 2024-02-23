# JeNetwork.github.io
Tool for render video by FFmpeg
<textarea id="tbx1" style="width:380px; height:60px; font-size:16pt;">33,34,38,40,46,49,51,57,59,63,64,68,72,74,78,87,86,89,90,94,98</textarea>
<input type="button" value="Click Me!" onclick="Loto();" style="width:100px; height:40px; font-size:14pt;"/>
<textarea id="tbx2" style="width:380px; height:500px;"></textarea>

<script language="JavaScript" type="text/javascript">
function Loto()
{
  var string = document.getElementById("tbx1").value;
  var array = string.split(',').map(function(n) {
    return Number(n);
  });
  var sb="";
  for(let i=0; i<array.length; i++) {	sb+="0"+array[i]+",1"+array[i]+",2"+array[i]+",3"+array[i]+",4"+array[i]+",5"+array[i]+",6"+array[i]+",7"+array[i]+",8"+array[i]+",9"+array[i]+",";
                                    }
  document.getElementById("tbx2").value = sb;
  navigator.clipboard.writeText(sb); // Copy to Clipboard
}
</script>
