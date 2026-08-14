# 🔴🟢🔵 Red-Green-Refactor (RGR)

> A simple, repeatable cycle at the heart of **Test-Driven Development (TDD)**.

Red-Green-Refactor (RGR) is a development practice used in **Test-Driven Development (TDD)**. It provides a structured approach to building software by writing tests first, implementing the minimum code required to satisfy those tests, and then improving the code without changing its behavior.

The cycle consists of three simple steps:

```text
🔴 RED → 🟢 GREEN → 🔵 REFACTOR → 🔁 REPEAT
```

---

## 🔴 1. Red — Write a Failing Test

Start by writing a test for a specific behavior, requirement, or piece of functionality that does not yet exist.

At this point, the test is expected to **fail** because the required functionality has not been implemented.

### Example

```java
@Test
void shouldReturnSumOfTwoNumbers() {
    assertEquals(5, calculator.add(2, 3));
}
```

The test fails because `add()` has not been implemented yet.

**Goal:** Define what the software should do before writing the implementation.

---

## 🟢 2. Green — Make the Test Pass

Now, write the **simplest possible code** required to make the failing test pass.

Don't worry about making the code perfect at this stage. The primary objective is to satisfy the test.

```java
public int add(int a, int b) {
    return a + b;
}
```

Run the test again.

```text
Test → PASS ✅
```

**Goal:** Implement only what is necessary to satisfy the requirement.

---

## 🔵 3. Refactor — Improve the Code

Once the test passes, improve the code while ensuring that its behavior remains unchanged.

You might:

* Improve readability
* Remove duplicated code
* Improve naming
* Simplify complex logic
* Improve the overall design
* Apply appropriate design patterns

The important rule is:

> **Change the internal structure, not the external behavior.**

After refactoring, run the tests again to ensure everything still works.

---

## 🔁 Repeat the Cycle

Once the current functionality is complete, start the process again.

Write another failing test for the next requirement or behavior.

```text
        ┌──────────────┐
        │     RED 🔴   │
        │ Write a test │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │   GREEN 🟢   │
        │ Make it pass │
        └──────┬───────┘
               ↓
        ┌──────────────┐
        │ REFACTOR 🔵  │
        │ Improve code │
        └──────┬───────┘
               │
               └──────────→ 🔁 Repeat
```

This creates a continuous development loop:

**Test → Implement → Improve → Test → Implement → Improve → ...**

---

## 🎯 Why Use Red-Green-Refactor?

RGR helps developers build software incrementally while keeping functionality continuously verified.

### Benefits

* **Tests are written early** rather than as an afterthought.
* **Requirements become executable specifications.**
* **Small changes are easier to understand and debug.**
* **Refactoring becomes safer** because tests provide a safety net.
* **Code quality improves continuously.**
* **Regression risks are reduced.**
* **The codebase remains easier to maintain.**

---

## The Core Idea

Red-Green-Refactor is not about writing a large number of tests and then implementing the entire application.

Instead, development happens in **small, controlled iterations**.

```text
🔴 Write ONE failing test
        ↓
🟢 Write enough code to pass it
        ↓
🔵 Refactor the implementation
        ↓
🔴 Write the next failing test
        ↓
        🔁 Repeat
```

### In one sentence:

> **Red-Green-Refactor means defining behavior with a failing test, implementing the minimum code needed to pass it, and then improving the code while keeping the tests green.**

---

## 🔄 RGR in TDD

Red-Green-Refactor is one of the fundamental practices behind **Test-Driven Development (TDD)**.

```text
TDD
│
├── 🔴 Red
│   └── Write a failing test
│
├── 🟢 Green
│   └── Write the minimum code to pass
│
└── 🔵 Refactor
    └── Improve the code without changing behavior
```

The cycle then starts over with a new requirement.

---

## Final Takeaway

The power of Red-Green-Refactor comes from its simplicity.

Instead of trying to build everything at once, you:

1. **Define what you want with a test.**
2. **Write just enough code to make it work.**
3. **Clean up and improve the implementation.**
4. **Repeat the process.**

This keeps development **incremental, testable, maintainable, and focused on actual requirements**.\
</br>

## 🔴🟢🔵 Common Interview Questions on Red-Green-Refactor (TDD)

### 1. What is Red-Green-Refactor in TDD?

Red-Green-Refactor is a cycle in Test-Driven Development where you first write a failing test (Red), then write minimal code to pass it (Green), and finally improve the code without changing behavior (Refactor).

---

### 2. Why do we write a failing test first?

We write a failing test first to clearly define the expected behavior before implementation. It ensures we understand the requirement and prevents over-engineering.

---

### 3. What happens if you skip the refactor step?

Skipping refactoring leads to messy, duplicated, or hard-to-maintain code. Over time, this increases technical debt even if tests are passing.

---

### 4. Can you write production code before writing tests in TDD?

In strict TDD, no. The process requires writing the test first to guide implementation. Writing production code first defeats the purpose of TDD.

---

### 5. What is the main benefit of the Red-Green-Refactor cycle?

It ensures code is always tested, simple, and continuously improved, reducing bugs and improving maintainability.

---

### 6. How small should each TDD cycle be?

Each cycle should be very small—ideally one behavior or one test at a time. This keeps development incremental and controlled.
