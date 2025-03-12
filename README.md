# Al-junaid-tech-phpTask2
Tasks may include developing applications,  writing scripts for data processing, creating  dynamic content, or building APIs
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Task 2</title>
</head>
<body>
<?php

// Create an indexed array of 10 random numbers (1-100)
$random_numbers = [];
for ($i = 0; $i < 10; $i++) {
    $random_numbers[] = rand(1, 100);
}

echo "<div style='font-family: Arial, sans-serif; padding: 20px; background-color: #f4f4f4;'>";
echo "<h2 style='color: blue;'>Task 1 part 1<br><br>Random Number Operations</h2>";

echo "<p><strong>Original Array:</strong> <span style='color: #007bff;'>" . implode(", ", $random_numbers) . "</span></p>";

// Find and display the sum of all numbers
$sum_of_numbers = array_sum($random_numbers);
echo "<p><strong>Sum of all numbers:</strong> <span style='color: #28a745;'>" . $sum_of_numbers . "</span></p>";

// Remove duplicate values from the array
$unique_numbers = array_unique($random_numbers);
echo "<p><strong>Array without duplicates:</strong> <span style='color: #dc3545;'>" . implode(", ", $unique_numbers) . "</span></p>";

// Find and display the maximum and minimum values from the array
if (!empty($random_numbers)) {
    $max_number = max($random_numbers);
    $min_number = min($random_numbers);
    echo "<p><strong>Maximum value:</strong> <span style='color: #ffc107;'>" . $max_number . "</span></p>";
    echo "<p><strong>Minimum value:</strong> <span style='color: #17a2b8;'>" . $min_number . "</span></p>";
} else {
    echo "<p style='color: red;'>Array is empty, cannot find max or min.</p>";
}

// Sort the array in ascending order and print it
sort($random_numbers);
echo "<p><strong>Sorted Array:</strong> <span style='color: #6c757d;'>" . implode(", ", $random_numbers) . "</span></p>";

echo "</div>";

?>
<?php

// Create an associative array named $employees
$employees = [
    "Alice" => 60000,
    "Bob" => 55000,
    "Charlie" => 75000,
    "David" => 62000,
    "Eve" => 70000,
];

echo "<div style='font-family: Arial, sans-serif; padding: 20px; background-color: #f8f8f8; border: 1px solid #ddd;'>";

// Sort the array by salary in ascending order.
$salary_ascending = $employees;
asort($salary_ascending);
echo "<h2 style='color: #007bff;'>Task 1 part 2 <br><br>Sorted by Salary (Ascending)</h2>";
echo "<div style='background-color: #e6f7ff; padding: 10px; border-radius: 5px; margin-bottom: 15px;'>";
foreach ($salary_ascending as $name => $salary) {
    echo "<p><strong>" . htmlspecialchars($name) . ":</strong> $" . number_format($salary) . "</p>";
}
echo "</div>";

// Sort the array by employee names in descending order.
$name_descending = $employees;
krsort($name_descending);
echo "<h2 style='color: #28a745;'>Sorted by Name (Descending)</h2>";
echo "<div style='background-color: #e8f5e9; padding: 10px; border-radius: 5px; margin-bottom: 15px;'>";
foreach ($name_descending as $name => $salary) {
    echo "<p><strong>" . htmlspecialchars($name) . ":</strong> $" . number_format($salary) . "</p>";
}
echo "</div>";

// Display the employee with the highest salary.
$highest_salary = max($employees);
$highest_paid_employee = array_search($highest_salary, $employees);

echo "<h2 style='color: #ffc107;'>Employee with Highest Salary</h2>";
echo "<div style='background-color: #fff3cd; padding: 10px; border-radius: 5px; margin-bottom: 15px;'>";
echo "<p><strong>Name:</strong> " . htmlspecialchars($highest_paid_employee) . "</p>";
echo "<p><strong>Salary:</strong> $" . number_format($highest_salary) . "</p>";
echo "</div>";

echo "</div>";

?>

<?php

// Create a multidimensional array to store book details
$books = [
    [
        "title" => "The Hitchhiker's Guide to the Galaxy",
        "author" => "Douglas Adams",
        "price" => 15.99,
    ],
    [
        "title" => "Pride and Prejudice",
        "author" => "Jane Austen",
        "price" => 12.50,
    ],
    [
        "title" => "1984",
        "author" => "George Orwell",
        "price" => 18.75,
    ],
];

// Access and update the price of the second book
$books[1]["price"] = 13.99;

// Print all book details in a structured format
echo "<h2>Task 1 part 3</h2>";
echo "<table style='border-collapse: collapse; width: 100%;'>";
echo "<tr><th style='border: 1px solid #ddd; padding: 8px;'>Title</th><th style='border: 1px solid #ddd; padding: 8px;'>Author</th><th style='border: 1px solid #ddd; padding: 8px;'>Price</th></tr>";

foreach ($books as $book) {
    echo "<tr>";
    echo "<td style='border: 1px solid #ddd; padding: 8px;'>" . htmlspecialchars($book["title"]) . "</td>";
    echo "<td style='border: 1px solid #ddd; padding: 8px;'>" . htmlspecialchars($book["author"]) . "</td>";
    echo "<td style='border: 1px solid #ddd; padding: 8px;'>$" . number_format($book["price"], 2) . "</td>";
    echo "</tr>";
}

echo "</table>";

?>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    .style{
        color:azure;
    }
</style>
<body>
<?php

// Create an associative array of five students
$students = [
    "Mishal" => 85,
    "Ramsha" => 65,
    "Hina" => 92,
    "Dania" => 58,
    "Alina" => 38,
];
echo "<h2>Task 2 part 1</h2>";
echo "<div style='background-color: lightblue;display:flex; width:500px;hight:800px; padding:30px; text-align:center;'>";

echo "<div style='background-color: lightpink;display:grid; width:200px; text-align:center;'>";
// Display each student's name and marks using foreach loop
echo "<h2>Student Marks:</h2>";
foreach ($students as $name => $marks) {
    echo "<p><strong>" . htmlspecialchars($name) . ":</strong> " . $marks . "</p>";
}

echo "</div>";
echo "<div style='background-color: azure;display:grid; width:200px; text-align:center;'>";
// Find and display the student who scored the highest marks
$highest_marks = max($students);
$highest_scorer = array_search($highest_marks, $students);

echo "<h2>Highest Scorer:</h2>";
echo "<p><strong>" . htmlspecialchars($highest_scorer) . ":</strong> " . $highest_marks . "</p>";
echo "</div>";
echo "<div style='background-color: red;display:grid; width:200px; text-align:center;'>";
// Identify and display the names of students who scored less than 50
echo "<h2>Students with Marks Below 50:</h2>";
$failed_students = [];
foreach ($students as $name => $marks) {
    if ($marks < 50) {
        $failed_students[] = htmlspecialchars($name);
    }
}

if (!empty($failed_students)) {
    echo "<p>" . implode(", ", $failed_students) . "</p>";
} else {
    echo "<p>No students scored below 50.</p>";
}
echo "</div>";
echo "</div><br>";
?>
<?php
echo "<h2>Task 2 part 2</h2>";
echo "<div style='background-color: pink; width:400px;font-size:30px;'>";
function generateFibonacci($count) {
    $fibonacci = [];
    if ($count <= 0) {
        return $fibonacci;
    }

    $fibonacci[0] = 0;

    if ($count > 1) {
        $fibonacci[1] = 1;
    }

    for ($i = 2; $i < $count; $i++) {
        $fibonacci[$i] = $fibonacci[$i - 1] + $fibonacci[$i - 2];
    }

    return $fibonacci;
}

$fibonacciSeries = generateFibonacci(10);

echo "First 10 Fibonacci numbers: <br>";
foreach ($fibonacciSeries as $number) {
    echo $number . ", ";
}
echo"</div>";
echo PHP_EOL; // Add a newline character
?>
<?php
echo "<h2>Task 2 part 3</h2>";

if (isset($_GET['number'])) {
    $n = intval($_GET['number']); // Get number from query string and convert to integer

    if ($n > 0) { // Check if the number is positive
        echo "<h2>Multiplication Table of " . $n . "</h2>";
        echo "<div style='background-color:pink;color:black;font-size:20px; border-radius:9px; width:500px; text-align:center;'>";
         $i = 1;
        while ($i <= 10) {
            $result = $n * $i;
            echo "<p>" . $n . " x " . $i . " = " . $result . "</p>";
            $i++;
        }
    } else {
        echo "<p>Please enter a positive number.</p>";
    }
    echo "</div>";
} else {
    ?>
    <form method="get">
        <label for="number">Enter a number:</label>
        <input type="number" name="number" id="number" required>
        <button style="background-color:white;color:darkblue; border-radius:9px;" type="submit">Generate Table</button>
    </form>
    <?php
}

?>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
<?php
echo "<h2>Task 3 part 1</h2>";
if (isset($_POST['marks'])) {
    $marks = intval($_POST['marks']);

    if ($marks >= 0 && $marks <= 100) {
        if ($marks >= 90) {
            $grade = "A+";
        } elseif ($marks >= 80) {
            $grade = "A";
        } elseif ($marks >= 70) {
            $grade = "B";
        } elseif ($marks >= 60) {
            $grade = "C";
        } else {
            $grade = "FAIL";
        }

        echo "<h2>Grade: " . $grade . "</h2>";
    } else {
        echo "<p>Please enter marks between 0 and 100.</p>";
    }
} else {
    ?>
    <form method="post">
        <label for="marks">Enter Marks (0-100):</label>
        <input type="number" name="marks" id="marks" required>
        <button type="submit">Calculate Grade</button>
    </form>
    <?php
}

?>

</body>
</html>





<!DOCTYPE html>
<html>
<head>
    <title>Paragraph Processor</title>
</head>
<body>
<!DOCTYPE html>
<html>
<head>
<title>Paragraph Processor</title>
</head>
<body>
<h1>Paragraph Analysis</h1>
<form method="post" action="">
    <textarea name="paragraph" rows="10" cols="50" placeholder="Enter your paragraph here (minimum 500 words)"></textarea><br>
    <input type="submit" value="Analyze">
</form>
</body>
</html>
        <?php


function processParagraph($paragraph) {
     // Basic word count estimation for 500 words check
     $estimatedWordCount = str_word_count($paragraph);

     if ($estimatedWordCount < 500) {
         echo "<p style='color:red;'>Warning: The paragraph does not appear to contain at least 500 words. It contains approximately " . $estimatedWordCount . " words.</p>";
         return; // Stop further processing if word count is insufficient
     }
 
     // 1. Count Words (accurate count)
     $words = str_word_count($paragraph, 1);
     $wordCount = count($words);
 
     // 2. Find Most Repeated Word (case-insensitive)
    $wordFrequency = array_count_values(array_map('strtolower', $words));
    arsort($wordFrequency);
    // Corrected line:
    $mostRepeatedWord = array_key_first($wordFrequency);

// 3. First and Last Words
$firstWord = reset($words);
$lastWord = end($words);

// Display Results
echo "<p>Word Count: " . $wordCount . "</p>";
echo "<p>Most Repeated Word: " . $mostRepeatedWord . "</p>";
echo "<p>First Word: " . $firstWord . "</p>";
echo "<p>Last Word: " . $lastWord . "</p>";
}

// Handling form submission
if (isset($_POST['paragraph'])) {
$paragraph = $_POST['paragraph'];
processParagraph($paragraph);
}

?>


<!-- // function processParagraph($paragraph) {
//     // Basic word count estimation for 500 words check
//     $estimatedWordCount = str_word_count($paragraph);

//     if ($estimatedWordCount < 500) {
//         echo "<p style='color:red;'>Warning: The paragraph does not appear to contain at least 500 words. It contains approximately " . $estimatedWordCount . " words.</p>";
//         return; // Stop further processing if word count is insufficient
//     }

//     // 1. Count Words (accurate count)
//     $words = str_word_count($paragraph, 1);
//     $wordCount = count($words);

//     // 2. Find Most Repeated Word (case-insensitive)
//     $wordFrequency = array_count_values(array_map('strtolower', $words));
//     arsort($wordFrequency);
//     $mostRepeatedWord = key(reset($wordFrequency));

//     // 3. First and Last Words
//     $firstWord = reset($words);
//     $lastWord = end($words);

//     // Display Results
//     echo "<p>Word Count: " . $wordCount . "</p>";
//     echo "<p>Most Repeated Word: " . $mostRepeatedWord . "</p>";
//     echo "<p>First Word: " . $firstWord . "</p>";
//     echo "<p>Last Word: " . $lastWord . "</p>";
// }

// // Handling form submission
// if (isset($_POST['paragraph'])) {
//     $paragraph = $_POST['paragraph'];
//     processParagraph($paragraph);
// }
// -->


