##Grade

|    |Possible|Earned|Category     | Objective                                          | 
|:--:|:------:|:----:|:-----------:|----------------------------------------------------|
|![2]|    10  |   0   | OGR Command | Ogr command was present.                          |
|![2]|    40  |   0   | OGR Command | Ogr command was syntactically correct.            |
|    |        |      |             |                                                    |
|![2]|    10  |   0   | Table Structure | Table structure was present.                  |
|![2]|    40  |   0   | Table Structure | Table structure was correct.                  |
|    | Total  |      |             |                                                    |
|    |    100 |   **0**   | Table Structure | Table structure was present, and correct.     |



![1] = Correct <br>
![2] = Incorrect <br>
![3] = Partially Correct <br>

[1]: https://raw.githubusercontent.com/rugbyprof/5443-Spatial-Database/master/media/correct.png
[2]: https://raw.githubusercontent.com/rugbyprof/5443-Spatial-Database/master/media/incorrect.png
[3]: https://raw.githubusercontent.com/rugbyprof/5443-Spatial-Database/master/media/partial.png

5443-Spatial-Databases
======================

5443-Spatial-Databases
`````
Assignment2
`````

`````
In this we are just checking the weather we are connect to the database and reterving the data from the database
below code displays and imports connects to the database
`````
<?php
$con=mysqli_connect("localhost","snaveen","Naveen@123","snaveen");
// Check connection
if (mysqli_connect_errno()) {
  echo "Failed to connect to MySQL: " . mysqli_connect_error();
}
$result = mysqli_query($con,"SELECT * FROM probes");

echo "<table border='1'>
<tr>
<th>name</th>
<th>yr</th>
<th>dest</th>
</tr>";
while($row = mysqli_fetch_array($result)) {
  echo "<tr>";
  echo "<td>" . $row['name'] . "</td>";
  echo "<td>" . $row['Yr'] . "</td>";
  echo "<td>" . $row['dest'] . "</td>";
  echo "</tr>";
}
echo "</table>";
mysqli_close($con);
?>

````
Output
````

name	yr	dest
pioneer 5	1960	sun
Mariner	1974	Mercury
Messenger	2008	Mercury
Zond	1964	Venus
Viking	1976	Mars
cassini	2000	Jupiter
Galileo	1995	Jupiter
