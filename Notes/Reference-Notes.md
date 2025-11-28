# EXPLORATORY TESTING MAP

Exploratory testing is about learning the system while questioning it.
Documenting what you see, what you test, and what you question. Shows:

- What areas exist in the product

- What risks live in those areas

- What ideas you intend to explore

- How you learn as you test

## FORMAT:

### 1. CHARTER
A single sentence defining what you're exploring and why.
**Format it as**: "Explore [area] to discover [information]."

### 2. TEST IDEAS
The mental models and test approaches you'll use. 
List specific heuristics (SFDPOT, Goldilocks, boundary analysis, etc.) or test idea patterns relevant to your charter.

### 3. EXECUTION NOTES
Actual areas/features/scenarios you covered during the session. 
Be specific about what you did, the data you used, and configurations tried.

### 4. BUGS/ISSUES FOUND
Problems discovered with enough detail to act on.
Include severity/priority indicators.

### 5. QUESTION/RISKS/FOLLOW-UPS
Things that need investigation, clarification from developers, or deeper testing later. 
Include blockers that stopped you from testing certain areas. 


# TEST CASE 

A step by step instructions. Shows repeatable instructions.
They are useful for:

- Regression
- Automation coverage
- Compliance and audit-heavy environments

## FORMART:
- **Test ID**: Unique identifier (e.g., TC-LOGIN-001)
- **Title**: Brief description of what's being tested
- **Priority**: How critical is this functionality? (High/Medium/Low)
- **Preconditions**: What must be true before starting
- **Test Steps**: Numbered, specific actions
- **Expected Results**: What should happen after each step or at the end
- **Actual Results**: Filled in during execution (leave blank for now)
- **Status**: Pass/Fail/Blocked (leave blank for now)