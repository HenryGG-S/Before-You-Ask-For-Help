# Before You Ask for Help: A Debugging Checklist for CS Students - Free Sample

Version: v0.1-beta  
Feedback: https://forms.gle/YOUR-FEEDBACK-FORM

## Start here

When your code breaks, your first job is not to guess harder. Your first job is to make the problem smaller and clearer.

Use this sample when you feel stuck, panicked, or unsure what to try next.

This does not do your coursework for you. It helps you understand and debug your own code more clearly.

## Panic checklist

- [ ] Copy the exact error message before changing anything.
- [ ] Find the file name and line number. Open that file and read the line above too.
- [ ] Classify the problem: syntax, name/scope, type, file/path, logic, Git, environment.
- [ ] Reproduce it once. Do not fix a bug you cannot make happen again.
- [ ] Shrink the problem: comment out unrelated code or test one tiny input.
- [ ] Check your most recent change. Bugs usually live near the last thing you edited.
- [ ] Add one observation at a time: print a variable, inspect a type, or run one test.
- [ ] Write the bug in plain English: "I expected X, but got Y, when I did Z."
- [ ] Prepare a minimal example before asking for help.

## Five common beginner errors

### Python: SyntaxError: invalid syntax

**What it usually means:** Python could not understand the structure of the line it points at, or sometimes the line just before it.

**Why beginners hit it:** Beginners often miss brackets, quotes, colons, commas, or close a string too early.

**Tiny broken example:**

```text
if score > 40
    print('pass')
```

**Tiny fixed example:**

```text
if score > 40:
    print('pass')
```

**What to check next:** Check the line above the arrow first. Look for missing colons, unclosed strings, or mismatched brackets.

**What to Google if still stuck:** `Python SyntaxError invalid syntax colon if statement`

**When to ask for help:** Ask for help if you can show the exact error, the five lines around it, and what you expected to happen.

### Python: IndentationError: expected an indented block

**What it usually means:** Python expected code to be nested under something like if, for, while, def, or class.

**Why beginners hit it:** Python uses indentation as part of the language, unlike Java or C which use braces.

**Tiny broken example:**

```text
if logged_in:
print('Welcome')
```

**Tiny fixed example:**

```text
if logged_in:
    print('Welcome')
```

**What to check next:** After a line ending in a colon, the next meaningful line usually needs to be indented.

**What to Google if still stuck:** `Python IndentationError expected an indented block`

**When to ask for help:** Ask for help if your editor shows mixed tabs/spaces or indentation looks correct but Python disagrees.

### Python: NameError: name is not defined

**What it usually means:** Python reached a name it does not know about yet.

**Why beginners hit it:** The variable may be misspelled, created inside a different scope, or used before assignment.

**Tiny broken example:**

```text
total = price + postage
print(totla)
```

**Tiny fixed example:**

```text
total = price + postage
print(total)
```

**What to check next:** Compare spelling exactly. Python treats total, Total, and totla as different names.

**What to Google if still stuck:** `Python NameError name is not defined variable scope`

**When to ask for help:** Ask for help if the variable is created inside a function, loop, or if block and you are unsure where it exists.

### Python: TypeError: unsupported operand type(s)

**What it usually means:** You are using an operation on values that do not fit together, such as adding a string to an integer.

**Why beginners hit it:** Input often arrives as text, even when it looks like a number.

**Tiny broken example:**

```text
age = input('Age: ')
print(age + 1)
```

**Tiny fixed example:**

```text
age = int(input('Age: '))
print(age + 1)
```

**What to check next:** Print type(value) for the variables involved. Do not guess the type.

**What to Google if still stuck:** `Python TypeError unsupported operand type string int`

**When to ask for help:** Ask for help if you are unsure which part of the expression has the wrong type.

### Python: IndexError: list index out of range

**What it usually means:** You asked for an item position that does not exist in the list.

**Why beginners hit it:** Beginners often forget that indexes start at 0, so the last item is len(items) - 1.

**Tiny broken example:**

```text
names = ['Ada', 'Grace']
print(names[2])
```

**Tiny fixed example:**

```text
names = ['Ada', 'Grace']
print(names[1])
```

**What to check next:** Print len(list_name) and the index you are using immediately before the failing line.

**What to Google if still stuck:** `Python IndexError list index out of range len index starts at zero`

**When to ask for help:** Ask for help if the index is calculated in a loop and only fails sometimes.

## Bug report template

Copy and fill this in before asking for help:

```text
What I was trying to do:

What I expected to happen:

What actually happened:

Exact error message:

Smallest code that reproduces it:

What I have already tried:

What I am still confused about:
```

## What the full beta includes

The paid beta includes the full debugging process, 20 common error explanations, a printable checklist, a bug report template, and a debugging worksheet.
