# Calculator Tool

## Overview
The Calculator Tool is a Python-based utility within the Atomic Agents ecosystem designed for performing a variety of mathematical calculations. It supports basic arithmetic operations such as addition, subtraction, multiplication, and division, as well as more complex operations including exponentiation and trigonometric functions.

## Installation
You can install the tool using any of the following options:

1. Using the CLI tool that comes with Atomic Agents. Simply run `atomic` and select the tool from the list of available tools. After doing so you will be asked for a target directory to download the tool into.
2. Good old fashioned copy/paste: Just like any other tool inside the Atomic Forge, you can copy the code from this repo directly into your own project, provided you already have atomic-agents installed according to the instructions in the main [README](/README.md).

## Input & Output Structure

### Input Schema
- `expression` (str): Mathematical expression to evaluate. For example, '2 + 2'.

### Output Schema
- `result` (str): Result of the calculation.

## Usage

Here's an example of how to use the Calculator Tool:

```python
from tool.calculator import CalculatorTool, CalculatorToolConfig

# Initialize the tool
calculator = CalculatorTool(config=CalculatorToolConfig())

# Define input data
input_data = CalculatorTool.input_schema(
    expression="sin(pi/2) + cos(pi/4)"
)

# Perform the calculation
result = calculator.run(input_data)
print(result)  # Expected output: {"result":"1.70710678118655"}
```

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes with clear messages.
4. Open a pull request detailing your changes.

Please ensure you follow the project's coding standards and include tests for any new features or bug fixes.

## License

This project is licensed under the same license as the main Atomic Agents project. See the [LICENSE](LICENSE) file in the repository root for more details.
