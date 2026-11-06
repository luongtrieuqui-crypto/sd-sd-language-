# Learn Sd in Vietnamese: A practical course

This course is designed for beginners and as a durable practice reference. Each lesson states a goal, explains the code, and gives exercises and self-checks. The examples use the Sd syntax implemented by this repository's IDE; Sd is not C/C++.

## Setup

1. Open `Sd IDE.html` in a browser.
2. Select **Mở tệp** and open a file from `examples/sd/`.
3. Select **Chạy**. If an error appears, inspect the **Vấn đề** tab and its line number.
4. Copy a sample before experimenting so that you can compare it with the original.

Sd statements in the samples end with `ed`. A program starts with `sta(main){` and closes the main block with `}`. The current examples include `imp*ioprt.ed` for I/O.

## Lesson 1 — Your first program

Open [`01_hello_world.sd`](../../examples/sd/01_hello_world.sd). It prints a line of text. Change the quoted string and run the program again.

Identify three parts: the import line, the `main` block, and the `pri` print statement. Text strings are enclosed in double quotes.

**Practice:** print your name and an introduction using two separate `pri` statements.

**Check yourself:** does changing the string change the output? Which token terminates an Sd statement?

## Lesson 2 — Integer variables

Open [`02_basic_math.sd`](../../examples/sd/02_basic_math.sd). Variables `a`, `b`, and `tong` store integers. A declaration and initial value use this form: `iid: sta(int name) => edt: sta(name = expression) ed`. After declaration, use the variable name in expressions and output statements.

Example:

```text
iid: sta(int a) => edt: sta(a = 12) ed
iid: sta(int b) => edt: sta(b = 8) ed
iid: sta(int tong) => edt: sta(tong = a + b) ed
iid: sta(pri) tong ed
```

The IDE interpreter supports basic arithmetic operators `+`, `-`, `*`, `/`, and `%`. Use parentheses to make grouping explicit. Integer division follows the interpreter's integer-division behavior.

**Exercise:** calculate the difference, product, and remainder of `a` and `b`. Store each result in its own variable, then print a label and its value.

**Check yourself:** is every variable declared before its first use? Is its name spelled consistently?

## Lesson 3 — Follow execution order

The interpreter executes statements from top to bottom inside `main`. Declare values first, calculate next, and print last. If an expression depends on another variable, create that variable before the expression uses it.

**Extension exercise:** write a small purchase-total program with `so_luong`, `don_gia`, `tam_tinh`, `phi`, and `tong_tien`. Multiply quantity by unit price, then add the fee. Print each component so the result can be checked.

Organize the program into three sections: input/data declarations, calculations, and output. This structure stays understandable when you later add a tax or discount.

## Lesson 4 — Strings and readable output

`pri` can print a quoted string or a variable/expression. Until you use the IDE's supported formatting features, print a descriptive label and the value on separate lines.

```text
iid: sta(pri) "Tong tien:" ed
iid: sta(pri) tong_tien ed
```

**Exercise:** update the purchase-total program to print clear labels for quantity, unit price, subtotal, fee, and total. Run the program after a few edits rather than changing everything before the first test.

## Lesson 5 — Common errors and diagnosis

- **Missing `ed`:** check the end of each `iid:` statement.
- **Misspelled variable:** compare spelling and letter case at declaration and use sites.
- **Undeclared variable:** add a declaration before the first expression that uses it.
- **Division by zero:** check the denominator before running a division.
- **Malformed program structure:** check `sta(main){` and the closing `}`.
- **No output:** confirm the intended file is open and select **Chạy**; inspect **Vấn đề**.

The IDE also supports stepping through execution and viewing variables. Click a line number to set a breakpoint, select **Gỡ lỗi**, and inspect the variables after each step.

## Capstone — Rectangle report

Create `examples/sd/04_rectangle_report.sd`:

1. Declare positive length and width values.
2. Calculate perimeter with `2 * (length + width)`.
3. Calculate area with `length * width`.
4. Print a report title, both dimensions, perimeter, and area.
5. Try two pairs of dimensions and verify the results by hand.

## Where to go next

After variables, expressions, and output, study conditions, loops, functions, and data structures in the reference materials in the repository root. Confirm advanced syntax against the specification and IDE rather than assuming it matches another language. See [`docs/README.md`](../README.md) for the documentation index and [`CODE_GUIDE.en.md`](../../CODE_GUIDE.en.md) for the IDE overview.
