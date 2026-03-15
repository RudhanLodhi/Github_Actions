## This is the python app 1

## Activity to Understand GitHub Workflow

This activity helps you practice creating Python code, writing unit tests, and automating test execution with GitHub Actions.

### Phase 2: Create Python Code and Tests

1. Add dependencies in requirements.txt:
	- pandas
	- pytest
2. Create folders:
	- src
	- tests
3. Create src/math_operations.py with:
	- add(a, b) -> returns a + b
	- sub(a, b) -> returns a - b
4. Create tests/test_operation.py and import:
	- from src.math_operations import add, sub
5. Add test cases:
	- test_add() with:
	  - assert add(2, 3) == 5
	  - assert add(-1, 1) == 0
	- test_sub() with:
	  - assert sub(5, 3) == 2
	  - assert sub(4, 3) == 1
	  - assert sub(3, 3) == 0
	  - assert sub(2, 3) == -1

### Phase 3: Set Up GitHub Actions Workflow

1. Create workflow file at .github/workflows/python-app.yml.
2. Set workflow name to Python CI.
3. Trigger workflow on:
	- push to main
	- pull_request to main
4. Add a test job:
	- runs-on: ubuntu-latest
5. Add steps:
	- Checkout code using actions/checkout@v2
	- Setup Python using actions/setup-python@v2 with python-version: '3.8'
	- Install dependencies:
	  - python -m pip install --upgrade pip
	  - pip install -r requirements.txt
	- Run tests with pytest

### Git Commands Used in This Activity

1. git add .
2. git commit -m "Unit test case updated"
3. git push origin main

By completing this activity, i learned how code changes can automatically trigger tests in GitHub Actions.
