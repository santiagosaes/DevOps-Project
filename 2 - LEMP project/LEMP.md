Project LEMP


Password for SQL 'PassWord.1'

CREATE USER 'santiagosaes'@'localhost' IDENTIFIED BY 'Sse_16078225';


Create table

CREATE TABLE LEMP_database.todo_list (item_id INT AUTO_INCREMENT, content VARCHAR(255), PRIMARY KEY(item_id));

Insert a few rows of content in the test table. You might want to repeat the next command a few times, using different VALUES:

INSERT INTO LEMP_database.todo_list (content) VALUES ("My first SQL query");

To confirm that the data was successfully saved to your table, run:

SELECT * FROM LEMP_database.todo_list;  






<?php
$user = "example_user";
$password = "password";
$database = "example_database";
$table = "todo_list";

try {
  $db = new PDO("mysql:host=localhost;dbname=$database", $user, $password);
  echo "<h2>TODO</h2><ol>";
  foreach($db->query("SELECT content FROM $table") as $row) {
    echo "<li>" . $row['content'] . "</li>";
  }
  echo "</ol>";
} catch (PDOException $e) {
    print "Error!: " . $e->getMessage() . "<br/>";
    die();
}