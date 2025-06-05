# 🧠 Prompting Techniques & Strategies

A comprehensive guide to effective prompt engineering strategies and code refactoring techniques for AI-assisted development.

## 📋 Table of Contents

- [Prompt Engineering Strategies](#-prompt-engineering-strategies)
- [Refactoring Prompts](#-refactoring-prompts)
- [When to Refactor](#-when-to-refactor)
- [Best Practices](#-best-practices)

## 🎯 Prompt Engineering Strategies

### Strategy #1: Q&A Strategy Prompt
**Use Case:** Getting tailored recommendations through guided questioning

```
@workspace propose a file/folder structure for this project. Ask me a series of yes/no questions that will help you provide a better recommendation.
```

**When to use:** When you need personalized suggestions and want the AI to gather context before providing recommendations.

---

### Strategy #2: Pros and Cons Prompt
**Use Case:** Evaluating different implementation approaches

```
What are a few different ways that I can implement this db connection logic. Give me the pros and cons of each strategy @file.
```

**When to use:** When you need to compare multiple approaches and understand trade-offs before making a decision.

---

### Strategy #3: Stepwise Chain of Thought Prompt
**Use Case:** Controlled, incremental code changes

```
Help me refactor the code in @file. Go one step at a time. Do not move to the next step until I give you the keyword "next". Begin.
```

**When to use:** When you want to maintain control over the refactoring process and review each change before proceeding.

---

### Strategy #4: Role Prompt
**Use Case:** Interactive learning and teaching scenarios

```
You are a skilled instructor who makes complex topics easy to understand. You come up with fun exercises so that your students can learn by doing. Your goal is to teach students to be proficient with regex. Move one step at a time and wait for the student to provide the correct answer before you move on to the next concept. If the student provides the wrong answer, give them a hint.
```

**When to use:** When you want to learn a new concept through guided practice and interactive feedback.

## 🔧 Refactoring Prompts

### Short Prompt
For quick, focused refactoring:

```
Refactor this code to reduce line count while maintaining readability and functionality. Focus on extracting repetitive patterns into reusable functions.
```

### Comprehensive Refactoring Prompt
For thorough code improvement:

```
Please refactor this code with the following objectives:

• Identify and extract duplicate or similar logic into reusable functions or methods
• Refactor repetitive patterns into more efficient abstractions
• Apply design patterns appropriate for your language/framework to consolidate similar functionality
• Move utility functions to separate files/modules and import them when needed
• Use higher-order functions to replace repeated code blocks
• Leverage language-specific features like list comprehensions, ternary operators, or destructuring to write more concise code
• Simplify nested conditionals using early returns, guard clauses, or the strategy pattern
• Break down large classes/files into smaller, more focused components with single responsibilities
```

## 🚦 When to Refactor

### ✅ You SHOULD Refactor When:
- **Performance Issues:** Code is slow and you plan to add significant functionality
- **Complex UI:** Multiple tabs or complex interface elements
- **Multiple Responsibilities:** Single files/components handling multiple pieces of functionality
- **Future Expansion:** You know you'll be building on this code extensively

### ❌ You SHOULD NOT Refactor When:
- **Feature Complete:** The feature is finished and working
- **Minimal Future Changes:** You don't expect to add much more functionality
- **Time Constraints:** Each refactor requires significant testing time

## 💡 Best Practices

### General Guidelines
- **Test After Refactoring:** Each refactor requires retesting everything
- **Incremental Approach:** Make small, focused changes rather than large overhauls
- **Documentation:** Update comments and documentation after refactoring

### Prompt Engineering Tips
- **Be Specific:** Provide clear context and constraints in your prompts
- **Use File References:** Tag relevant files with `@file` for better context
- **Iterative Approach:** Use stepwise prompts for complex changes
- **Role Definition:** Define the AI's role when you need specific expertise

### Code Quality Indicators
- **Readability:** Code should be easy to understand
- **Maintainability:** Changes should be easy to implement
- **Performance:** Refactored code should maintain or improve performance
- **Testability:** Code should be easy to test and debug

---

*Remember: The goal of both prompting and refactoring is to create maintainable, efficient code while minimizing development friction.*
