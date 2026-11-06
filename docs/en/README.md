# Learn Sd / Sd++ (English)

Welcome! This page is the English learning path and documentation index for this repository. Sd/Sd++ use project-specific syntax and are **not C/C++**. The browser IDE in this repository contains the interpreter used by these examples.

- [Hướng dẫn học bằng tiếng Việt](../vi/README.md)
- [English project home](../../README.md)
- [Documentation index](../README.md)

## 1. Get started

1. Open [`Sd IDE.html`](../../Sd%20IDE.html) in a modern browser.
2. Select **Open file** and load a `.sd` or `.sdpp` sample from `examples/`.
3. Select **Run** to execute, or **Debug** to step through the program.
4. If the program uses `ipt`, enter input in the **Input** tab and run it again.

Current examples:

- [Sd: Hello World](../../examples/sd/01_hello_world.sd) and [basic math](../../examples/sd/02_basic_math.sd).
- [Sd++: Hello World](../../examples/sdpp/01_hello_world.sdpp), [basic math](../../examples/sdpp/02_basic_math.sdpp), and [rectangle area](../../examples/sdpp/03_rectangle_area.sdpp).
- [Examples index](../../examples/README.md).

## 2. Recognize the two syntaxes

| | Sd | Sd++ |
|---|---|---|
| Program start | `sta(main){` | `ssta {` and a `define [...]` block |
| Print statement | `iid: sta(pri) ... ed` | `ids.pri: ... $` |
| Variable declaration | `iid: sta(int x) ... ed` | `iptedt.int x ... $` |
| Statement terminator | `ed` | `$` |
| File ending | Close the block with `}` | End the file with `##` |
| Extension | `.sd` | `.sdpp` |

These are the conventions supported by the IDE interpreter in this repository. Use the included samples as the source of truth when writing new code.

## 3. Suggested learning path

1. **Run your first program:** open Hello World and change its string.
2. **Variables and arithmetic:** inspect `02_basic_math` for each syntax; try changing values and operators.
3. **Control flow:** study conditional and loop forms in the reference materials, then add each exercise as a separate sample file.
4. **Functions, data structures, and libraries:** learn these from the original textbook/specification and validate syntax in the IDE before expanding examples.
5. **Debugging:** click a line number to add a breakpoint, start Debug, and inspect the Variables and Issues tabs.

Do not assume that familiar syntax from another language is supported. Verify it against repository examples or the language specification.

## 4. Reference materials

Original documents remain in the repository root to preserve existing links:

- LaTeX textbook: [`Giáo_Trình_Master_...tex`](../../Gia%CC%81o_Tri%CC%80nh_Master_La%CC%A3%CC%82p_Tri%CC%80nh_Sd_va%CC%80_Sd___tu%CC%9B%CC%80_Co%CC%9B_Ba%CC%89n_%C4%91e%CC%82%CC%81n_Na%CC%82ng_Cao.tex).
- LaTeX technical specification: [`Đặc_tả_Kỹ_thuật_...tex`](../../%C4%90a%CC%A3%CC%86c_ta%CC%89_Ky%CC%83_thua%CC%A3%CC%82t_To%CC%82%CC%81i_cao_va%CC%80_Ca%CC%82%CC%89m_nang_Toa%CC%80n_die%CC%A3%CC%82n_Ngo%CC%82n_ngu%CC%9B%83_Sd_va%CC%80_Sd__.tex).
- The `.txt` specification notes and PDF textbook are also in the root; the PDF is currently named `giaotrinhsd:sdpp.pdf`.
- [English IDE code guide](../../CODE_GUIDE.en.md).

## 5. Add and organize lessons

- Put Sd examples in `examples/sd/`, using names such as `04_loops.sd`.
- Put Sd++ examples in `examples/sdpp/`, using names such as `04_loops.sdpp`.
- Keep each program/lesson in its own file; use lowercase, ASCII names with an order number.
- Update the README in the relevant examples folder when adding a lesson.
- Do not mix file extensions or the `ed`, `$`, and `##` terminators between syntaxes.

## 6. Common troubleshooting

- **Syntax error:** check the correct program wrapper, closing braces, and terminators for that language.
- **No output:** confirm the intended file is open and Run was selected; check the Issues tab.
- **Missing input:** add another line in the Input tab.
- **Finding a file:** use the [`docs/README.md`](../README.md) index or GitHub repository search.
