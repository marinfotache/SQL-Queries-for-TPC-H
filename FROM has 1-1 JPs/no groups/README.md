
### Parameters defining the current scenario are:
    * FROM has 1-1 JPs
    * no groups
    

### Here is a typical query of this scenario:<br>



 SELECT MIN(region.r_regionkey) AS MIN__region__r_regionkey<br>FROM<br>&emsp; region  <br>OFFSET 743 <br>LIMIT 379


<br><br>

### ... and a "lengthier" one:
<br>


 SELECT MAX(LTRIM(region.r_comment)) AS MAX__LTRIM__region__r_comment<br>FROM<br>&emsp; region  <br>OFFSET 959 <br>LIMIT 896

