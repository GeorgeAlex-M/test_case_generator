# test_case_generator
Test cases generator script written in python-OOP

This code defines a number of classes for representing configuration data, test techniques, test cases, and a test case generator.

The Config class has two attributes: test_techniques and output_path. test_techniques is a list of TestTechnique objects, and output_path is a string representing the path where the generated test cases will be written to an Excel file.

The TestTechnique class has several attributes: technique_type, technique, name, description, num_test_cases, coverage, and inputs. technique_type and technique are both strings representing the type and name of the test technique. name and description are also strings, representing the name and description of the test technique. num_test_cases is an integer representing the number of test cases to be generated for this test technique. coverage is a string representing the coverage provided by this test technique. inputs is a list of inputs to be used when generating test cases for this test technique.

The TestCase class has three attributes: test_case_num, technique, and input. test_case_num is an integer representing the number of the test case. technique is a string representing the name of the test technique used to generate this test case. input is a string representing the input used for this test case.

The TestCaseGenerator class has one attribute: config, which is an instance of the Config class. It has two methods: generate_test_cases and write_to_excel. generate_test_cases generates a list of TestCase objects based on the test techniques and inputs specified in the configuration data. write_to_excel writes the generated test cases to an Excel file at the path specified in the configuration data.
