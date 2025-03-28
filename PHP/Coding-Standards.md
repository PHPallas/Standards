code: SWDA-0018  version: **1.0**  status: **active**

---
# PHP Coding Standard

This document outlines the PHP Coding Standards for the PHPallas team. It establishes best practices and guidelines to ensure consistency, readability, and maintainability in PHP code. Contributors are expected to adhere to these standards in all PHP projects.

## Version Support
- PHP scripts **MAY** support PHP 5.3 and later. However, they **SHOULD** support PHP 7.0 and later. All scripts **MUST** support PHP version 8.0 and later.

## Code Structure

- Opening braces `{` for classes, methods, and control structures (such as `if`, `for`, `while`, etc.) **MUST** be placed on a new line.
  
- Closing braces `}` **MUST** also be on a new line, aligned with the corresponding opening statement.

- Each control structure **MUST** be clearly separated by a blank line for readability.

## Indentation and Spacing

- Contributors **MUST** use consistent indentation for nested structures. Four-space indentation is **RECOMMENDED**. Tabs **MUST NOT** be used.

- Contributors **MUST** include a single space between keywords and the opening parenthesis in control structures (e.g., `if`, `for`, `while`).

- There **MUST NOT** be any space between the function name and the opening parenthesis.

- Contributors **MUST** keep lines of code to a reasonable length (80 characters is **RECOMMENDED**) for better readability. Lines **MUST** not exceed 120 characters.

## Documentation and Comments

- All classes, methods, and functions **SHOULD** be documented using PhpDoc blocks.

- Contributors **MAY** use comments to explain complex logic. However, comments **MUST** be placed above the code they describe.

## Naming Conventions

- Contributors **MUST** use PascalCase for class names, and class names **SHOULD** be self-descriptive.

- Contributors **MUST** use camelCase for variables, class properties, class methods, and function names. All names **SHOULD** be self-descriptive.

- Constant names **MUST** follow MACRO_CASE.

- In the case of associative arrays, array keys **MUST** be in camelCase.

- Object properties and methods **MUST** be in camelCase.

## File Structure

- Each PHP file **SHOULD** contain only one class definition, and the file name **MUST** match the class name.

- PHP files **MUST** use only `<?php` and `<?=` tags.

- Files **MUST** use UTF-8 without BOM.

- A file **SHOULD** declare new symbols (classes, functions, constants, etc.) and cause no other side effects, or it **SHOULD** execute logic with side effects, but **SHOULD NOT** do both.

- Namespaces and classes **MUST** follow the autoloading PSR-4 standard.

## Arrays

- All arrays **MUST** have a trailing `,`.

## Additional Best Practices

- **Error Handling**: Contributors **SHOULD** implement error handling using exceptions instead of relying on error suppression.

- **Type Hinting**: Contributors **SHOULD** use type hinting for function parameters and return types to improve code clarity and reliability. If an inline hint is not available, for example in case of supporting PHP 5.3 ~ 5.6, PhpDoc type hinting **MUST** be placed.

- **Dependency Management**: Contributors **MUST** use Composer as a defacto approach for dependency management and include a `composer.json` file in the project root.

- **Testing**: Contributors **MUST** write unit tests for their code using PHPUnit to ensure functionality and reliability.

## Example Code

Below is an example compliant with the PHP Coding Standards targeting PHP 5.3+:

```php
<?php

namespace SomeName\YetAnotherName;

/**
 * Class ExampleClass
 *
 * This class serves as an example to demonstrate the use of PhpDoc
 * and coding standards. It contains a constant, a property, and a method
 * that illustrates basic functionality.
 */
class ExampleClass
{
    /**
     * Constant EXAMPLE_CONST
     *
     * This constant holds a sample value that can be used throughout the class.
     * It is defined as a string.
     */
    const EXAMPLE_CONST = "value";

    /**
     * @var mixed $exampleProperty
     *
     * This property is an example variable that can hold any type of data.
     * It is publicly accessible and can be modified or read from outside the class.
     */
    public $exampleProperty;

    /**
     * Method exampleMethod
     *
     * This method takes a parameter and checks its value.
     * It prints a message to the output based on whether the parameter is true or false.
     *
     * @param bool $param A boolean value that determines the output message.
     *
     * @return void
     */
    public function exampleMethod($param)
    {
        // Check if the provided parameter is true
        if ($param)
        {
            // Output message indicating the parameter is true
            echo "Parameter is true.";
        }
        else
        {
            // Output message indicating the parameter is false
            echo "Parameter is false.";
        }
    }
}

// Create an instance of ExampleClass
$example = new ExampleClass();

// Call the exampleMethod with a boolean value of true
$example->exampleMethod(true);

// Example associative array demonstrating usage of camelCase keys
$exampleArray = array (
    "someProperty" => false,
    "someAnotherProperty" => true,
);

```

And below code is another example targeting 8.0 +:

```php
<?php

declare(strict_types=1);

namespace SomeName\YetAnotherName;

use Vendor\ExampleInterface;
use Vendor\ExampleAbstractClass;

/**
 * Class ExampleClass
 *
 * This class serves as an example to demonstrate the use of PhpDoc
 * and coding standards. It contains a constant, a property, and a method
 * that illustrates basic functionality.
 */
class ExampleClass extends ExampleAbstractClass implements ExampleInterface
{
    /**
     * Constant EXAMPLE_CONST
     *
     * This constant holds a sample value that can be used throughout the class.
     * It is defined as a string.
     */
    public const EXAMPLE_CONST = "value";

    /**
     * @var mixed $exampleProperty
     *
     * This property is an example variable that can hold any type of data.
     * It is publicly accessible and can be modified or read from outside the class.
     */
    public mixed $exampleProperty;

    /**
     * Method exampleMethod
     *
     * This method takes a parameter and checks its value.
     * It prints a message to the output based on whether the parameter is true or false.
     *
     * @param bool $param A boolean value that determines the output message.
     *
     * @return void
     */
    public function exampleMethod(bool $param): void
    {
        // Check if the provided parameter is true
        if ($param)
        {
            // Output message indicating the parameter is true
            echo "Parameter is true.";
        }
        else
        {
            // Output message indicating the parameter is false
            echo "Parameter is false.";
        }
    }
}

// Create an instance of ExampleClass
$example = new ExampleClass();

// Call the exampleMethod with a boolean value of true
$example->exampleMethod(true);

// Example associative array demonstrating usage of camelCase keys
$exampleArray = [
    "someProperty" => false,
    "someAnotherProperty" => true,
];


```