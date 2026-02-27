# Development

## Rules of Development

### Formatting and Style

#### Markdown

##### Syntax

---

- (**Level**) `#` for chapter titles, `##` for sections, `###` for subsections, `####` for subsubsections, and at most `#####` allowed.

---

- (**Bold**) Use `**Text**` for important terms or definitions.
- Example: **Postulate 1**: The state of a quantum system is described by a wavefunction.

---
  
- (**Italics**) Use `*Text*` for emphasis.
- Example: *The Schrödinger equation* governs the time evolution of quantum states.

---

- (**Items**)
- Use `-` for unordered (forbidden to use `+`，`*`) and `1.`, `2.` (or all use `1`), etc. for ordered lists.
- Example:
- **Unordered List**:
  - Item 1
  - Item 2
- **Ordered List**:
     1. First step
     2. Second step
     3. XXX
     4. YYY
     5. ZZZ
     6. AAA

---

- (**Code**) Use templates like:

  ````markdown{.line-numbers}
  ```language{.line-numbers}
  Code block
  ```
  ````

  to format code snippets, with `language` for syntax highlighting.

- Example:

    ```python{.line-numbers}
    def my_function():
        print("Hello World")
    ```

---

- (**Links**) Use `[Text](URL)` for hyperlinks. Use `<URL>` for plain URLs.
  - Example: [CriticalLine's GitHub](https://github.com/CriticalLine)
  - Example: <https://www.example.com>

---

- (**Images**) Use `![Figure Index: Captain](Image URL)` for images.
  - Example:
  ![Figure 1-1: XBOX](https://www.microsoftestore.com.hk/resource/images/cms/explore_microsoft/2020/11/06/a68beb04-6b24-490d-87ae-09f87aed4601.jpg)

---

- (**Equations**) Use LaTeX syntax for inline equations `\( E = mc^2 \)` and display equations `\[ E = mc^2 \]`. Forbidden to use `$ equation $` and `$$ equation $$` syntax.
  - Example: The energy-mass equivalence is given by \( E = mc^2 \).

---

- (**Tables**) Use Markdown table syntax for tabular data.
  - Example:
  
    | Column 1 | Column 2 | Column 3 |
    |----------|----------|----------|
    | Data 1   | Data 2   | Data 3   |
    | Data 4   | Data 5   | Data 6   |

---

- (**Task Lists**) Use `[ ]` for incomplete tasks and `[x]` for completed tasks.
  - Example:
    - [ ] Write introduction
    - [x] Define scope

---

- (**Diffs**) Use `diff` syntax for code changes, with `-` for deletions and `+` for additions.
  - Example:

```diff
function calculateTotal(items) {
-   let total = 0;
+   let total = 0.0;
    
    for (let item of items) {
-       total += item.price;
+       total += parseFloat(item.price);
    }
    
+   // Round to 2 decimal places
+   total = Math.round(total * 100) / 100;
    return total;
}
```

---

- (**Mermaid Diagrams**) Use Mermaid syntax for diagrams.
  - Example:

    ```mermaid
      graph TD
          A[Begin] --> B{Condition}
          B -->|Yes| C[Execute Operation A]
          B -->|No| D[Execute Operation B]
          C --> E[End]
          D --> E
      ```

    ```mermaid
        classDiagram
        classA <|-- classB : implements
        classC *-- classD : composition
        classE o-- classF : aggregation
      ```

---

- (**Comments**) Use `<!-- Comment -->` for comments that will not be rendered in the final output.
  - Example: <!-- This is a comment and will not appear in the rendered document -->

---

- (**Vector/Matrix**) Use LaTeX syntax for matrices. Only use `\begin{bmatrix} ... \end{bmatrix}` for matrices, and `\begin{pmatrix} ... \end{pmatrix}` is forbidden.
  - Example: Hilbert matrix \( H_n \) is defined as:
    \[
    H_n = \begin{pmatrix}
    1           & \frac{1}{2}    & \dots & \frac{1}{n}    \\
    \frac{1}{2} & \frac{1}{3}    & \dots & \frac{1}{n+1}  \\
    \vdots      & \vdots         & \ddots& \vdots         \\
    \frac{1}{n} & \frac{1}{n+1}  & \dots & \frac{1}{2n-1}
    \end{pmatrix}
    \]

---

- (**Escape**) Use `\` to escape special characters when necessary.
  - Example: To display \*, use `\*` to escape it.
  - Example: To display \\, use `\\` to escape it.
  - Example: To display \#, use `\#` to escape it.
  - Example: To display \$, use `\$` to escape it.

❌Forbidden: Footnotes, all kinds of horizontal line `---`.

##### Style Guidelines

#### html/css/js/ts

#### LaTex
