This document serves as the complete definition of Altair's coding standards 
for source code. This document not only contains the specific guidelines that must be followed,
but also includes reccomendations for compliance.

Make sure you read through this document carefully.

## Table of Contents

1. [General Rules](#general-rules)
2. [Language Standards](#language-standards)
3. [Naming Convention](#naming-convention)
4. [Classes](#classes)
5. [Methods](#methods)
6. [Comments](#comments)
7. [Testing Code](#testing-code)
8. [Documentation](#documentation)

## General Rules

- **NEVER** Hard Code!
- If we must release quick but not quite right code, refactor the code ASAP. (Don't go into technical debt)
- However, abide by the 5 minute rule and try to do things right the first time. (Fix code that takes 5m or less)
- Don't repeat yourself
- Don't have unnecessary code
- Avoid Global Variables
- Peer review code before pushing to production
- Centralize, discuss, and share code knowledge
- Write sustainable, scalable code
- Use a descriptive folder structure using thoughtful separation of code.

## Language Standards

- Avoid in-line styling in Javascript and CSS.
  - Always use separate file for CSS.
- Keep database queries in the model instead of the UI.
- Use single quotes as default.
  - Only use double quotes when quoting single quotes.

## Naming Convention

1. In General:
   - Class names must be written in `UpperCamelCase`
2. File Names:
   - File names must be written in `snake_case`
   - Name files based on `object_action`
     - > File: customer_add.py
3. CSS:
   - Classes must be written in `dash-case`
4. PHP:
   - Variables and Method names must be written in `lowerCamelCase`
   - Constants must be written in `CONSTANT_CASE`
5. Python:
   - Everything except Class names must be written in `snake_case`
6. SQL:
   - No hyphens
   - Database names and Table names must be written in `snake_case`
     - `Database_name`
     - `table_name`, `field_name`

## Classes

- Each Class should have its own separate file.
- Don't use inheritance
- Keep It Simple, Stupid

## Methods

- Methods should not have too many parameters. (4 is typically too much)
  - If more, think about using an array.
- Methods should have one objective.
- The bodies of methods should be 30 lines.
- Avoid deep nesting.
- Create Variables as close to where it will be used.
- In PHP, verbose 'if' statements can be switches.
- In Python, verbose 'if' statements can be changed to a dictionary type for similar functionality.

## Comments

Comments are not allowed in production code.
  - Temporary comments are allowed around code that will be used later, but make sure to add a descriptor line. (No left-over code commented out)

## Testing Code

- Test code often (DevOps, Py test)
- Validate success using try/catch (try/except) and use custom error handling, but afterwards keep error syntax from showing (especially if client-facing).
- Use dependency injection to aid in testing by allowing us to know immediately what the dependencies are.

## Documentation

- Create documentation with the end user in mind.
  - Credit Bureau
  - API Client
  - Internal Functionality
