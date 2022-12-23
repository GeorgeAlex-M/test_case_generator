# Test Case Generator
A Python library for generating and writing test cases to an Excel file.

# Installation
To install Test Case Generator, use pip:

```pip install test-case-generator```

# Dependencies
Test Case Generator requires the following Python packages:

```openpyxl```

# Usage
To use Test Case Generator, import the Config, TestTechnique, and TestCaseGenerator classes from the test_case_generator module:

```from test_case_generator import Config, TestTechnique, TestCaseGenerator```

# Configuring Test Techniques and Output Path
First, create a list of TestTechnique objects, each representing a test technique to be used when generating test cases. Each TestTechnique object has the following attributes:

```
technique_type (str): The type of test technique (e.g. "Boundary Value Analysis", "Equivalence Partitioning")
technique (str): The name of the test technique (e.g. "BVA", "EP")
name (str): The name of the test technique (e.g. "Test Technique 1", "Test Technique 2")
description (str): A description of the test technique
num_test_cases (int): The number of test cases to be generated for this test technique
coverage (str): The coverage provided by this test technique (e.g. "100%", "90%")
inputs (list): A list of inputs to be used when generating test cases for this test technique
```

Next, create an instance of the Config class, passing in the list of TestTechnique objects and the path to the output Excel file as arguments:

```
# Create a list of TestTechnique objects
test_techniques = [
    TestTechnique(technique_type="Boundary Value Analysis", technique="BVA", name="Test Technique 1", description="Test technique for testing boundary values", num_test_cases=5, coverage="100%", inputs=["input1", "input2", "input3"]),
    TestTechnique(technique_type="Equivalence Partitioning", technique="EP", name="Test Technique 2", description="Test technique for testing equivalence classes", num_test_cases=3, coverage="90%", inputs=["input4", "input5"])
]

# Create a Config object
config = Config(test_techniques=test_techniques, output_path="test_cases.xlsx")
```

# Generating and Writing Test Cases
To generate and write the test cases to the Excel file, create an instance of the TestCaseGenerator class, passing in the Config object as an argument. Then, call the write_to_excel method on the TestCaseGenerator object:

```
# Create a TestCaseGenerator object
generator = TestCaseGenerator(config)

# Generate and write the test cases to the Excel file
generator.write_to_excel()```

This will generate and write the test cases to the specified Excel file, using the test techniques and inputs specified in the configuration data.

# Example
Here's an example of how you might use Test Case Generator in your code:

```from test_case_generator import Config, TestTechnique, TestCaseGenerator

# Create a list of TestTechnique objects
test_techniques = [
    TestTechnique(technique_type="Boundary Value Analysis", technique="BVA", name="Test Technique 1", description="Test technique for testing boundary values", num_test_cases=5, coverage="100%", inputs=["input1", "input2", "input3"]),
    TestTechnique(technique_type="Equivalence Partitioning", technique="EP", name="Test Technique 2", description="Test technique for testing equivalence classes", num_test_cases=3, coverage="90%", inputs=["input4", "input5"])
]

# Create a Config object
config = Config(test_techniques=test_techniques, output_path="test_cases.xlsx")

# Create a TestCaseGenerator object
generator = TestCaseGenerator(config)

# Generate and write the test cases to the Excel file
generator.write_to_excel()```

This will generate and write the test cases to the specified Excel file, using the test techniques and inputs specified in the configuration data.

# License
Test Case Generator is licensed under the MIT License. See the LICENSE file for details.
