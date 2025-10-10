# Command: /generate-test-cases

Given the issue description below, generate potential test cases to validate the feature, bug fix, or enhancement.
Do **not** write the implementation — only suggest tests that a developer can execute.

### Input
$ARGUMENTS

### Instructions
1. Identify whether this issue is a bug, feature, refactor, or enhancement.
2. Generate **3–7 test cases** that would cover:
   - Functional behavior
   - Edge cases
   - Input validation or error handling
   - Integration points (if relevant)
3. For each test case, include:
   - **Title:** short descriptive name
   - **Description:** what the test validates
   - **Inputs / Preconditions:** any data or state required
   - **Expected Outcome:** what result or behavior is expected
4. If the issue description is missing critical information, include a **“Missing Info”** section with questions a developer should answer before writing tests.

### Output Format
**Issue Type:** Bug / Feature / Refactor / Enhancement

**Test Cases**
1. **Title:** ...
   - **Description:** ...
   - **Inputs / Preconditions:** ...
   - **Expected Outcome:** ...

**Missing Info**
- ...
