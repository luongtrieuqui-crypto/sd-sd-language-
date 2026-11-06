# Sd / Sd++ Code Guide

This guide explains the code present in the repository. The examples in `sdform.sd` and `shortsd.sd` use the project's own Sd syntax; they are **not C/C++ code**. Some examples are compressed onto a single line, so the notes below describe their visible structure and intent without claiming that every fragment is independently formatted or tested.

## 1. `Sd IDE.html` — browser IDE and interpreter

This is a self-contained browser application: `<style>` defines the presentation, `<div id="app">` lays out the interface, and `<script>` implements parsing and execution for Sd programs.

### User interface

- The toolbar provides run/debug, example and snippet selection, formatting, file open/save, and copy actions.
- The editor area combines line numbers, source editing, syntax highlighting, and error highlighting.
- The adjacent panel has tabs for output, variables, input, problems, and reference information.
- CSS variables and media queries support light/dark themes, smaller screens, and reduced-motion preferences.

### Language processing

- `SdFault` carries an error code, message, and source line so the IDE can report diagnostics at a useful location.
- `stripComments`, `tokenize`, class `P`, and `parseExpr` handle comments, tokenization, and expression parsing.
- `Prog` parses Sd program structures such as functions, data structures, control-flow statements, and imports.
- `PProg` extends the parser for Sd++, including preprocessing and that variant's additional constructs.
- `VM` executes parsed programs. It manages variables and scopes, function calls, expressions, input/output, pointers, heap operations, and safety limits.
- The IDE connects the parser and VM to the editor, panels, and debugger. Breakpoints and step controls let users inspect execution.

### Typical execution flow

1. Enter or open source code in the editor.
2. The IDE analyzes the source and displays diagnostics when it finds issues.
3. On run, the VM executes the program; input comes from the Input tab or an interactive prompt.
4. Output, errors, and variable/debug information appear in their corresponding panels.

## 2. `sdform.sd` and `shortsd.sd` — language examples

These files demonstrate Sd code. `shortsd.sd` packs multiple constructs onto a single line; `sdform.sd` includes comments that indicate the intended purpose of sections. Read them using Sd's own separators and keywords rather than substituting syntax from another language.

Constructs visible in the examples include:

- `imp...` — importing a library or file; the examples refer to I/O and mathematics libraries.
- A `diem` function definition and a `main` block — examples of function declaration and the program entry point.
- `int`, `float`, and `str` declarations — examples of typed data.
- `ipt` input and `pri` output statements.
- `for`, `while`, and conditional blocks — examples of control flow.
- A structure declaration and a `void` function — examples of data structures and a function without a return value.

The sample source combines constructs to illustrate syntax; do not assume every fragment is a standalone exercise or independently runnable. To verify a program, open it in `Sd IDE.html`, check the Problems tab, and run it.

## 3. Language reference materials

The `.tex`, `.txt`, and `.pdf` files provide the project's tutorials and reference material. Consult them to confirm exact syntax, statement terminators, data types, and differences between Sd and Sd++ before changing examples.

## 4. Scope of this guide

This guide explains the organization and apparent purpose of the repository code; it is not a complete Sd/Sd++ language specification. Some files are compressed, and the IDE interface and many diagnostics are currently in Vietnamese.
