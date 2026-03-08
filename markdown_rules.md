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

---

## Style Guidelines

---

Allowed colors of text (default = black): red, blue, green, coral
Not allowed: yellow, white

Example:
<span style="color:red;">TEST TEXT: You can use red for text.</span>
<span style="color:blue;">TEST TEXT: You can use blue for text.</span>
<span style="color:green;">TEST TEXT: You can use green for text.</span>
<span style="color:coral;">TEST TEXT: You can use coral for text.</span>

Allowed colors of background: yellow (=<mark></mark>), lime, cyan, lightpink
Not allowed: blue, green, black, maroon, olive, teal, indigo, silver,

Example:
<span style="color:black;background-color:yellow;">TEST TEXT: You can use yellow for background.</span>
<span style="color:black;background-color:lime;">TEST TEXT: You can use lime for background.</span>
<span style="color:black;background-color:cyan;">TEST TEXT: You can use cyan for background.</span>
<span style="color:black;background-color:lightpink;">TEST TEXT: You can use light red for background.</span>

Waitlist of colors: chartreuse (lime), pink (lightpink), salmon (coral)

Not allowed both for text and background: brown, purple, grey, beige, salmon, navy, blackkhaki and all other colors not allowed above.

- (**Colored Text**) Use HTML `<span style="color:color;">Text</span>` for colored text, where `color` can be a color name or hex code.
  - Example: <span style="color:red;">This text is red.</span>
  1. (**Red**) Use red for warnings or important notes.
  1. (**Green**) Use green for positive outcomes or confirmations.
  1. (**Blue**) Use blue for informational text or references.
  1. (**Yellow**) Use yellow for cautionary notes or highlights.

- (**Colored text in KaTex**) Use `\color{color}{Text}` for colored text in KaTex, where `color` can be a color name or hex code.
  - Example: The equation \( \color{red}{E = mc^2} \) is famous.

<span style="color:black;background-color:orange;">Test text</span>
<span style="color:black;background-color:magenta;">Test text</span>
<span style="color:black;background-color:violet;">Test text</span>
<span style="color:black;background-color:gold;">Test text</span>
<span style="color:turquoise;">Test text</span>
<span style="color:black;background-color:plum;">Test text</span>
<span style="color:orchid;">Test text</span>
<span style="color:black;background-color:tan;">Test text</span>

---

-

<div style="padding: 15px; background-color: #E3F2FD; border-left: 5px solid #2196F3; margin: 15px 0;">
💡 Info: This is an informational box with custom styling to highlight important information.
</div>
<div style="padding: 15px; background-color: #FFF3E0; border-left: 5px solid #FF9800; margin: 15px 0;">
⚠️ Warning: This is a warning box used to alert users to important information.
</div>
<div style="padding: 15px; background-color: #F1F8E9; border-left: 5px solid #8BC34A; margin: 15px 0;">
✅ Success: This is a success box used to indicate successful operations.
</div>

<div style="padding: 15px; background-color: #FFEBEE; border-left: 5px solid #F44336; margin: 15px 0;">
❌ Error: This is an error box used to indicate problems or issues.
</div>

<div style="padding: 15px; background-color: #e6fffffe; border-left: 5px solid rgb(25, 247, 255); margin: 15px 0;">
  🆕 New Feature: This is a new feature box used to highlight newly added features.
</div>

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

- `[TOC]`should place the first line of the document before the `#` title.
-
