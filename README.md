# PHP Array Key Type Juggling Bug

This repository demonstrates a subtle bug in PHP related to how it handles array keys and type juggling.  The problem occurs when using large integer keys (outside the typical integer range) in arrays.  These large integer keys are implicitly converted into strings, leading to unexpected behavior in checks (like `isset()`) and iterations (like `foreach`).

The `bug.php` file shows the erroneous behavior, while `bugSolution.php` provides a solution and explanation.

## Bug Description

PHP's loose typing can cause unexpected results when using large integer keys for arrays.  The integer keys get implicitly cast to strings, which may not match your expectations when testing using `isset()` or iterating through the array using `foreach`.

## How to Reproduce

1.  Clone this repository.
2.  Run `bug.php` using a PHP interpreter.
3.  Observe the unexpected output.