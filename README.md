<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Exercise</title>
</head>
<body>
    <?php
    function calculateAverage($numbers) {
        $sum = array_sum($numbers);
        $count = count($numbers);
        if ($count > 0) {
            return $sum / $count;
        } else {
            return null; 
        }
    }

    $numbers = [1, 2, 3, 4, 5];
    
    echo "Array: " . join(", ", $numbers) . "<br>";
    echo "Average: " . calculateAverage($numbers) . "<br>"; 

    function isPalindrome($string) {
        $string = strtolower(preg_replace("/[^A-Za-z0-9]/", '', $string));
        $reverse = strrev($string); 
        return $string === $reverse;
    }

    $string = "A man, a plan, a canal, Panama!";
    echo "String: \"" . $string . "\"<br>";
    echo "Is Palindrome: " . (isPalindrome($string) ? 'true' : 'false') . "<br>"; 
    
    function generateFibonacci($terms) {
        $fibonacci = [0, 1];
        for ($i = 2; $i < $terms; $i++) {
            $fibonacci[$i] = $fibonacci[$i - 1] + $fibonacci[$i - 2];
        }
        return $fibonacci;
    }

    $terms = 10;
    echo "Terms: " . $terms . "<br>";
    echo "Fibonacci Sequence: [" . implode(", ", generateFibonacci($terms)) . "]<br>";
    ?>
</body>
</html>
