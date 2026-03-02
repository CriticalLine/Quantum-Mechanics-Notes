# Markdown Rules

## Syntax

HTML means when you use inline html in markdown, you need to use the corresponding syntax, otherwise, it cannot be rendered correctly. For example, for bold text, you need to use `<b>Text</b>` in inline HTML.

---

- (**Level**) `#` for chapter titles, `##` for sections, `###` for subsections, `####` for subsubsections, and at most `#####` allowed.

---

- (**Bold**) Use `**Text**` for important terms or definitions.
- (**HTML Bold**) `<b>Text</b>`
- Example: **Postulate 1**: The state of a quantum system is described by a wavefunction. <b>This wavefunction contains all the information about the system.</b>

---
  
- (**Italics**) Use `*Text*` for emphasis.
- (**HTML Italics**) `<i>Text</i>`
- Example: *The Schrödinger equation* governs the time evolution of quantum states. <i>It is a fundamental equation in quantum mechanics.</i>

---

- (**HTML Line Breaks**) Use `<br>` for line breaks in HTML.

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

    ```mermaid1
      graph TD
          A[Begin] --> B{Condition}
          B -->|Yes| C[Execute Operation A]
          B -->|No| D[Execute Operation B]
          C --> E[End]
          D --> E
    ```

    ```mermaid1
        classDiagram
        classA <|-- classB : implements
        classC *-- classD : composition
        classE o-- classF : aggregation
    ```

---

- (**Comments**) Use `<!-- Comment -->` for comments that will not be rendered in the final output.
  - Example: <!-- This is a comment and will not appear in the rendered document -->

---

- (**Vector/Matrix**) Use LaTeX syntax for matrices. Only use `\begin{bmatrix} ... \end{bmatrix}` for matrices, and `\begin{pmatrix} ... \end{pmatrix}` is prohibited.
  - Example: Hilbert matrix \( H_n \) is defined as:
    \[
    H_n = \begin{bmatrix}
    1           & \frac{1}{2}    & \dots & \frac{1}{n}    \\
    \frac{1}{2} & \frac{1}{3}    & \dots & \frac{1}{n+1}  \\
    \vdots      & \vdots         & \ddots& \vdots         \\
    \frac{1}{n} & \frac{1}{n+1}  & \dots & \frac{1}{2n-1}
    \end{bmatrix}
    \]

---

- (**Escape**) Use `\` to escape special characters when necessary.
  - Example: To display \*, use `\*` to escape it.
  - Example: To display \\, use `\\` to escape it.
  - Example: To display \#, use `\#` to escape it.
  - Example: To display \$, use `\$` to escape it.

---

- (**Table of Contents**) Use `[TOC]` to generate a table of contents based on the headings in the document.
  - Example:

[TOC]

---

❌Forbidden: Footnotes, all kinds of horizontal line `---`.

## Style Guidelines

---

Allowed colors of text: red,
Not allowed: yellow

Allowed colors of background:
Not allowed:

- (**Colored Text**) Use HTML `<span style="color:color;">Text</span>` for colored text, where `color` can be a color name or hex code.
  - Example: <span style="color:red;">This text is red.</span>
  1. (**Red**) Use red for warnings or important notes.
  1. (**Green**) Use green for positive outcomes or confirmations.
  1. (**Blue**) Use blue for informational text or references.
  1. (**Yellow**) Use yellow for cautionary notes or highlights.

- (**Colored text in KaTex**) Use `\color{color}{Text}` for colored text in KaTex, where `color` can be a color name or hex code.
  - Example: The equation \( \color{red}{E = mc^2} \) is famous.

<span style="color:red;">Test text测试文本</span>
<span style="color:blue;">Test text测试文本</span>
<span style="color:green;">Test text测试文本</span>
<span style="color:yellow;">Test text测试文本</span>
<span style="color:black;background-color:yellow;">Test text测试文本</span>=<mark>Text</mark>
<span style="color:purple;">Test text测试文本</span>
<span style="color:orange;">Test text测试文本</span>
<span style="color:black;background-color:pink;">Test text测试文本</span>
<span style="color:brown;">Test text测试文本</span>
<span style="color:gray;">Test text测试文本</span>
<span style="color:black;background-color:cyan;">Test text测试文本</span>
<span style="color:magenta;">Test text测试文本</span>
<span style="color:black;background-color:lime;">Test text测试文本</span>
<span style="color:maroon;">Test text测试文本</span>
<span style="color:navy;">Test text测试文本</span>
<span style="color:olive;">Test text测试文本</span>
<span style="color:teal;">Test text测试文本</span>
<span style="color:violet;">Test text测试文本</span>
<span style="color:indigo;">Test text测试文本</span>
<span style="color:gold;">Test text测试文本</span>
<span style="color:silver;">Test text测试文本</span>
<span style="color:coral;">Test text测试文本</span>
<span style="color:turquoise;">Test text测试文本</span>
<span style="color:salmon;">Test text测试文本</span>
<span style="color:plum;">Test text测试文本</span>
<span style="color:orchid;">Test text测试文本</span>
<span style="color:black;background-color:tan;">Test text测试文本</span>
<span style="color:black;background-color:blackkhaki;">Test text测试文本</span>
<span style="color:black;background-color:lavender;">Test text测试文本</span>
<span style="color:black;background-color:beige;">Test text测试文本</span>
<span style="color:mint;">Test text测试文本</span>delete
<span style="color:black;background-color:azure;">Test text测试文本</span>delete
<span style="color:black;background-color:chartreuse;">Test text测试文本</span>

---

-

---

- (**Progress Bars**) A progress bar can be used to indicate project completion status, it is better to use in developing notes and delete or comment out in the final version. Don't forget to adjust the width after development to reflect the actual progress.
  - Example:

<div style="margin: 20px 0;">
  <p><strong>Project Progress:</strong></p>
  <div style="background-color: #e0e0e0; border-radius: 5px; height: 20px;">
    <div style="background: linear-gradient(90deg, #4CAF50, #e1ffbf); width: 50%; height: 100%; border-radius: 5px; text-align: center; color: white; font-size: 12px; line-height: 20px;"> <!-- change width to control progress -->
      50%
    </div>
  </div>
</div>

---
