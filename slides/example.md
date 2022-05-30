---
theme: biodt
lang:  en
---

# BioDT Pandoc slide template {.title}

**Author, Affiliation**

# Text formatting {.section}
\

- Regular text, *text in italics*
- Text in ***bold italics***
- Text of a regular size,
  <small>text of a ***smaller*** size</small>.
- **Bold text** without italics
- [Link to tool used to produce these slides](https://github.com/csc-training/slide-template)

# Mathematics {.section}
\

### Equations
- Eq 1: $e = mc^2$
- Eq 2:
  $\frac{\partial^2 u}{\partial t^2} = c^2 \nabla^2 v$

### More equations 
- Eq 3 (centered):

$$\oint_{\partial \Sigma} E \cdot dl
    = - \int_\Sigma \frac{\partial B}{\partial t} \cdot d A$$

# Nested lists 1 {.section}
\

- The beginning of a list, marked by a filled circle.
    - A list item, marked by an open circle.
        - A sub-item of said item.

1. We can also create numbered lists, e.g. if we wanted several lists on a slide.
    - Under the list header, the first item marked by a filled circle.
        - And a sub-item marked by an open circle.

2. This is another numbered list.
    - And this, the first item of that list.

# Nested lists 2 {.section}
\

1. What if we wanted numbered sub-items within a numbered list? 
    - This is also possible:
        1. Sub-item 1
        2. Sub-item 2

2. Or other kinds of list variations?
    1. Now this item is numbered...
        * ... Whereas this one isn't.

- Then there's this one.
    1. I have a number!  
    2. So do I...
        1. Don't forget me!

# Definition list {.section}
\

A term of interest
  : A definition of that term

Another term of interest
  : To define this term, more text is needed.
  : In fact, we need two rows to do it.

# Function inputs and outputs {.section}
\

`Function(input1, input2, input3,` `output1`{.output}`)`

  : `input1`{.input}
    : If we wanted to make inputs and outputs easier to follow...

    `input2`{.input}
    : We could use different colours for...

    `input3`{.input}
    : Function inputs...

    `output1`{.output}
    : And function outputs

# Code examples {.section}
\

### Some code in boxes:
\

```python
import os

if os.path.isfile('foobar'):
    with open('foobar') as fp:
        txt = fp.read()
    print('File contents:')
    print(txt)
```

```c
#include <stdio.h> 

int square(x) {
    printf("Going to square value %d.", x);
    return x*x;
}
```

# Images {.section}
\

<p>
<img src="theme/biodt/img/biodt-twitter.png"> 
</p>

Screencap of the BioDT Twitter page.

<p align="center">
  <img src="theme/biodt/img/biodt-twitter.png" width="420" height="260" > 
</p>

<p align="center">
Same image, but centered and smaller.
</p>

# Columns 1 {.section}
\

<div class="column">
- We can create side-by-side columns
    - Here we have the first of two...
</div>

<div class="column">
- This might be useful e.g. if we have a large horizontal image under the text.
</div>

# Columns 2 {.section}
\

<div class="column">
- A second option is to split text and images by column.
    - Another chance to advertise the BioDT Twitter page... 
</div>

<div class="column">
<p>
<img src="theme/biodt/img/biodt-twitter.png"> 
</p>
</div>

# Tables 1 {.section}
\

#### The default table format looks like this:

\

|            |             | 1     | 2     | 4     | 8     |
| ---------- | ----------- | ----: | ----: | ----: | ----: |
| **Case 1** | vanilla     | 0.757 | 0.719 | 0.574 | 0.547 |
|            | *optimised* | 0.899 | 0.838 | 0.658 | 0.607 |
| **Case 2** | vanilla     | 1.252 | 1.111 | 0.684 | 0.756 |
|            | *optimised* | 1.443 | 1.277 | 0.748 | 0.818 |

# Tables 2 (highlights) {.section}
\

#### We can also highlight different values in tables:

\

|            |             | 1     | 2           | 4           | 8     |
| ---------- | ----------- | ----: | ----------: | ----------: | ----: |
| **Case 1** | vanilla     | 0.757 | 0.719       | 0.574       | 0.547 |
|            | *optimised* | 0.899 | 0.838       | 0.658       | 0.607 |
| **Case 2** | vanilla     | 1.252 | ***1.111*** | 0.684       | 0.756 |
|            | *optimised* | 1.443 | 1.277       | ***0.748*** | 0.818 |

# {.author}

