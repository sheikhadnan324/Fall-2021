<!DOCTYPE html>
<html>
<head>
 
    
    <title >Update Employee</title>
    
</head>
<body>
<?php
    require('db.php');
    
    if (isset($_REQUEST['username'])) {
        
        $ID = stripslashes($_REQUEST['ID']);
        $ID  = mysqli_real_escape_string($con, $ID);
        $Name   = stripslashes($_REQUEST['Name']);
        $Name    = mysqli_real_escape_string($con, $Name);
        $Department = stripslashes($_REQUEST['Department']);
        $Department= mysqli_real_escape_string($con, $Department);
        $JoiningDate = date("Y-m-d H:i:s");
        $query    = "UPDATE into `employee` (ID, Name, Department, JoiningDate)
                     VALUES ('" . md5($ID) . "', '$Name', '$Department', '$JoiningDate')";
        $result   = mysqli_query($con, $query);
        if ($result) {
            echo "<form>
                  <h3>You Update successfully.</h3><br/>
                  <p >Click here to <a href='search.php'>Search</a></p>
                  </form>";
        } else {
            echo "<form>
                  <h3>Required fields are missing.</h3><br/>
                  <p>Click here to <a href='update.php'>employee_update</a> again.</p>
                  </form>";
        }
    } else {
?>
    <form action="" method="post">
        <h1>Update</h1>
        <input type="number" class="update-input" name="ID" placeholder="ID" required /><br><br>
        <input type="text" class="update-input" name="Name" placeholder="Name"><br><br>
        <input type="text" class="update-input" name="Department" placeholder="Department"><br><br>
        <input type="Update" name="update" value="Update" class="Update-button"><br>
        <p><a href="update.php">Click to Update</a></p>
    </form>
<?phpin
    }
?>
</body>
</html>
