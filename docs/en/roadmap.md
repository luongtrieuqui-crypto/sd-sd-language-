# Sd / Sd++ learning roadmap (English)

This roadmap turns the repository into a long-term learning project. Each stage has a goal, expected outcome, and related files.

## Goal

- Learn the official Sd and Sd++ syntax used by the repository's browser IDE.
- Keep examples small, structured, and easy to compare.
- Teach users how to debug, modify, and extend examples without breaking the project.
- Turn the repo into a practical learning notebook rather than a loose collection of files.

## Stage 1 — Learn the IDE

- Goal: open files, run programs, read errors, and debug step by step.
- Files: `Sd IDE.html`, `README.md`, `README.vi.md`, `docs/README.md`.
- Outcome: the learner can open `.sd` and `.sdpp` files, inspect the issue tab, and run code in the interpreter.

## Stage 2 — Sd fundamentals

- Goal: understand imports, `main`, variables, arithmetic, and output.
- Samples: `examples/sd/01_hello_world.sd`, `02_basic_math.sd`.
- Exercises: add `03_input_output.sd`, `04_variable_math.sd`, and `05_report.sd`.

## Stage 3 — Sd++ fundamentals

- Goal: understand the `ssta` wrapper, `define`, `main`, `ids.pri`, typed variables, and `$` terminators.
- Samples: `examples/sdpp/01_hello_world.sdpp`, `02_basic_math.sdpp`, `03_rectangle_area.sdpp`.
- Exercises: add `04_output_format.sdpp`, `05_math_flow.sdpp`, and `06_report.sdpp`.

## Stage 4 — Branches and loops

- Goal: write conditional and repeated logic.
- Task: create example files for if/else and loop patterns in both `examples/sd/` and `examples/sdpp/`.
- Outcome: users can separate decision logic and repeated logic into readable blocks.

## Stage 5 — Functions and modular code

- Goal: split logic into functions / blocks and write clearer code.
- Practice: create `lesson_function.sd` and `lesson_function.sdpp` to demonstrate reusable logic.
- Rule: each function should solve one problem; variable names should explain their purpose.

## Stage 6 — Data structures and larger examples

- Goal: handle groups of values and build more realistic reports.
- Task: create examples about arrays, data tables, and summaries.
- Outcome: users can separate data, logic, and presentation.

## Stage 7 — Mini project work

Possible projects:

- Calculator
- Invoice total calculator
- Score report
- Student management demo

Each project should stay in its own file or its own folder so it is easy to run and compare.

## Naming rules for new lessons

- Use ordered names: `01_`, `02_`, `03_` ...
- Keep the topic short and clear: `math`, `loop`, `function`, `report`
- Use the correct extension: `.sd` and `.sdpp`
- Update the relevant README when new examples are added

## Final goal

The repository should become a reliable long-term learning environment: beginner-friendly, well organized, and easy to extend.
