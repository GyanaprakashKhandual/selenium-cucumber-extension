# Cucumber Step Definition Generator for Selenium Java

🚀 **Cucumber Step Definition Generator** is a VS Code extension that helps developers quickly generate **step definitions** for **Selenium Java** from selected Cucumber (Gherkin) steps.

## ✨ Features

- ✅ **Automatically Generates Step Definitions** for **Given, When, Then, And** steps.
- ✅ **Handles Multi-line Selections** and processes entire documents if no text is selected.
- ✅ **Removes Duplicates** and ensures unique step definitions.
- ✅ **Supports Parameterized Steps**:
  - Converts `"text"` values to `"([^"]*)"` for dynamic input handling.
  - Converts numbers like `123` to `(\\d+)`.
- ✅ **Valid Java Method Naming**:
  - Removes special characters.
  - Converts step text to snake_case Java methods.
  - Ensures unique method names by appending `_1`, `_2`, etc.
- ✅ **Copies Output to Clipboard** for easy pasting into step definition files.

---

## 📌 How It Works

1. **Select** Cucumber (Gherkin) steps in a `.feature` file.
2. **Run the Command**:
   - Open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P` on Mac).
   - Search for **"Generate Cucumber Step Definitions"** and run the command.
3. **Paste the Generated Code** in your step definition file.

---

## 🛠️ Example Usage

### **Cucumber Feature File (`.feature`)**
```gherkin
Feature: Login

  Scenario: Successful Login
    Given I am on the login page
    When I enter valid username and "password123"
    And I click on the login button
