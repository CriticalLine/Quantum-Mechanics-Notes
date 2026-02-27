# Development

## Rules of Development

### Formatting and Style

#### Markdown

##### Syntax

- (**Level**) `#` for chapter titles, `##` for sections, `###` for subsections, `####` for subsubsections, and at most `#####` allowed.
- (**Bold**) Use `**Text**` for important terms or definitions.
  - Example: **Postulate 1**: The state of a quantum system is described by a wavefunction.
- (Italics) Use `*Text*` for emphasis.
  - Example: *The Schrödinger equation* governs the time evolution of quantum states.
- (Items)
  - Use `-` for unordered (forbidden to use `+`，`*`) and `1.`, `2.` (or all use `1`), etc. for ordered lists.
  - Example:
    - **Unordered List**:
      - Item 1
      - Item 2
    - **Ordered List**:
      1. First step
      2. Second step
  1. XXX
  1. YYY
  1. ZZZ
  1. AAA
- (Code) Use

  ````markdown
  ```language
  Code block
  ```
  ````

  to format code snippets, with `language` for syntax highlighting.
  - Example:

    ```python
    def my_function():
        print("Hello World")
    ```

- (Links) Use `[Text](URL)` for hyperlinks.
  - Example: [CriticalLine's GitHub](https://github.com/CriticalLine)
- (Images) Use `![Figure Index: Captain](Image URL)` for images.
  - Example: ![Figure 1-1: Schrödinger's Cat](https://example.com/schrodingers_cat.png)
- (Equations) Use LaTeX syntax for inline equations `\( E = mc^2 \)` and display equations `\[ E = mc^2 \]`. Forbidden to use `$ equation $` and `$$ equation $$` syntax.
  - Example: The energy-mass equivalence is given by \( E = mc^2 \).
- (Tables) Use Markdown table syntax for tabular data.
- (Task Lists) Use `- [ ]` for incomplete tasks and `- [x]` for completed tasks.
  - Example:
    - [ ] Write introduction
    - [x] Define scope

#### html/css/js/ts

#### LaTex
