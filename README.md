## Python Test Framework for Automated Challenge Evaluation

A lightweight testing system that validates participant submissions against predefined challenges and generates Excel scorecards.

### Core Features

- **Challenge Validation**: Validates code execution results against expected outputs
- **Automated Reporting**: Generates Excel files with participant scores
- **Multi-Language Support**: Works with Python, Java, JavaScript, and other languages

### Required Files

<code>
// challenges.json structure
{
  "challenge1": {
    "function_name": "validate_challenge1",
    "test_cases": [
        [
          [900, 940, 950, 1100, 1500, 1800],
          [910, 1200, 1120, 1130, 1900, 2000]
        ],
        3
      ],
      [
        [
          [900, 940],
          [910, 1200]
        ],
        1
      ],
  }
}
</code>

### Prerequisites

`pip install openpyxl`

### Execution Workflow

1. **Directory Structure**
   <code>
   language_folder/
   ├── participant1/
   │ ├── challenge1/
   │ │ └── Solution.py
   │ └── challenge2/
   │ └── Solution.py
   └── participant2/
   ├── challenge1/
   │ └── Solution.py
   └── challenge2/
   └── Solution.py
   </code>

2. **Run Tests**

Windows

`python test_all.py`

Linux/macOS

`python3 test_all.py`

3. **Output**
   Generates `results.xlsx` with:

- Participant names
- Challenge-wise scores
- Overall performance metrics
