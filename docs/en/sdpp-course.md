# Learn Sd++ in English: A practical course

This course moves from file structure to variables and arithmetic, with guidance for practice and troubleshooting. Examples use the Sd++ syntax interpreted by this repository's IDE; this project syntax is not C++.

## Setup and file rules

Open `Sd IDE.html`, select **Open file**, and load a `.sdpp` file from `examples/sdpp/`. Select **Run** to execute it. Sample Sd++ files use an outer `ssta { ... }` wrapper, a `define [...]` block, `$` statement terminators, and `##` at the end of the file. Keep all of these markers in place.

## Lesson 1 — Program structure and output

Open [`01_hello_world.sdpp`](../../examples/sdpp/01_hello_world.sdpp). Read from the outside inward: `ssta {` opens the Sd++ section, `define` names the entry point, `main: {` opens the program body, `ids.pri:` prints a value, and the closing markers end the blocks and file.

**Practice:** change the greeting to your own sentence. Add another `ids.pri:` statement to print a second line. Run after each change.

**Check yourself:** does each statement end with `$`? Does the file end with `##`? Is the `main` block closed?

## Lesson 2 — Variables and arithmetic

Open [`02_basic_math.sdpp`](../../examples/sdpp/02_basic_math.sdpp). Declare and initialize an integer with `iptedt.int name = expression $`. Use its name in later expressions, then print it with `ids.pri:`.

```text
iptedt.int a = 12 $
iptedt.int b = 8 $
iptedt.int tong = a + b $
ids.pri: "Tong hai so la:" $
ids.pri: tong $
```

Basic arithmetic operators are `+`, `-`, `*`, `/`, and `%`. Use intermediate variables when they make each calculation easier to verify.

**Exercise:** add variables `hieu`, `tich`, and `thuong_nguyen`; calculate the difference, product, and integer quotient. Print a descriptive label for each result. Do not divide by zero.

## Lesson 3 — Organize calculations

A maintainable program separates data declarations, calculations, and output. Choose meaningful names such as `chieu_dai`, `chieu_rong`, and `dien_tich`. For a long expression, use intermediate variables and compare the result with a hand calculation.

**Exercise:** open [`03_rectangle_area.sdpp`](../../examples/sdpp/03_rectangle_area.sdpp), add the perimeter calculation `2 * (chieu_dai + chieu_rong)`, and print the result. Test multiple dimensions.

## Lesson 4 — Read errors and debug

- **Missing `$`:** ordinary Sd++ statements in these samples need a terminator.
- **Missing `##`:** keep it at the end of the file.
- **Undeclared variable:** declare a variable before using it in an expression.
- **Incorrect arithmetic:** check operator order and use small values you can calculate by hand.
- **No output:** confirm the intended file is open, select **Run**, and inspect the **Issues** tab.

Use **Debug** and a line-number breakpoint to inspect variables during execution. Fix one issue at a time and rerun to see exactly what changed.

## Capstone — Spending report

Create `examples/sdpp/04_budget_report.sdpp` with these steps:

1. Declare `so_luong`, `don_gia`, and `phi_van_chuyen`.
2. Calculate `tam_tinh = so_luong * don_gia`.
3. Calculate `tong_tien = tam_tinh + phi_van_chuyen`.
4. Print each value with a clear label.
5. Try quantity 1 and a larger quantity; verify both totals by hand.

## Add more lessons

Place programs in `examples/sdpp/` using an order number and topic, such as `05_expressions.sdpp`. Keep each file self-contained and update the folder README when adding a lesson. See the [documentation index](../README.md) and [English IDE code guide](../../CODE_GUIDE.en.md).

Learn advanced constructs such as conditions, loops, functions, and memory from the specification/textbook and validate them in the IDE. Do not assume their syntax matches C++.
