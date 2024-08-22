
## Jupiter notebooks Layout guide

When making your Jupyter notebook you should think of it as a Sub-Heading 2 of a chapter in the master report. This guide will help you to structure your Jupyter notebook for automatic integration with Microsoft word and the master report.

### Use of Heading 1

Heading 1 is reserved for chapters in the report document. Do not use a markdown heading 1 in your Jupiter notebooks.

### Use of Heading 2

Every Jupyter Notebook must begin with a markdown cell with a Heading 2. This should be the first cell in your Jupiter notebook. There should be nothing before the heading, this should be the only Heading 2 in your Jupyter Notebook.

For example:

```md
## EDA of Deaths by Region 2007-2020
```

The heading 2’s in the Jupiter notebooks will be a subheading for the chapters in the report

for example:

Chapter 3 Exploratory Data Analysis

3.1 A Heading 2 in the Word Document

3.2 *Heading 2 will be from notebook-01-eda-births-by-county-1985-2020.ipynb*

3.3 *Heading 2 will be from notebook-02-eda-births-deaths-marriages-1960-2021.ipynb*

3.4 *Heading 2 will be from notebook-03-eda-deaths-region-2007-2020.ipynb*

3.5 A Heading 2 in the Word Document

Chapter 4: Statistical Analysis

4.1 A Heading 2 in the Word Document

4.2 *Heading 2 will be from notebook-05-sa-births-by-county-1985-2020.ipynb*

4.3 *Heading 2 will be from notebook-06-sa-births-deaths-marriages-1960-2021.ipynb*

4.4 *Heading 2 will be from notebook-07-sa-deaths-region-2007-2020.ipynb*

4.5 A Heading 2 in the Word Document

Chapter 5: Machine Learning

### Heading in your Jupiter notebook

All other headings in the Jupiter notebooks are to be in markdown cell
and are to be headings 3, 4 or 5

```md
### Heading 3

#### Heading 4

##### Heading 5
```

### Heading number format

When your Jupiter notebook is merged with word document the Word document will automatically take responsibility for numbering the headings. Do not prefix any heading in your Jupiter notebook with section numbers or a section label.

Correct format example

```md
## EDA of births deaths marriages 1960 2021 file

### Setup

#### Create Data Frames
```

Bad example

```md
## Section 3.4: EDA of births deaths marriages 1960 2021 file

### 3.4.1 Setup

#### 3.4.2 Create Data Frames

```

### Paragraphs

Do not break up paragraphs with line breaks in your Jupiter notebook markdown cells. Only use a line break if you are intending to start a new paragraph. When the Jupiter notebook is merged with word it will automatically format the paragraph

Correct format example:

```md
Columns Statistics and UNIT are of no use as they only contain a single value.

VALUE which is the primary measure in the dataset only has values in 71149 and so we need to decide what to do with the NaNs.
```

Wrong format example:

```md
Columns Statistics and UNIT are of no use as they only contain a single value.

<line break in Jupyter that Word interpreted as a new paragraph>

VALUE which is the primary measure in the dataset only has values in 71149 and so we need <line break in Jupyter that Word interpreted as a new paragraph> to decide what to do with the NaNs.
```

### LaTeX Expressions

be aware that Latex expressions will not copy directly from Jupiter notebook and will have to be saved as an image first

### Images and Output

The output of all the cells in the Jupiter notebook graphs images table output will copy to the Word document automatically.

### Captions: Images, tables and other

Word cannot recognize a caption in an image and there is no automatic way to import a caption in the Microsoft Word format. To that end I have developed a workaround. Take the following image in cell `[43]` to add a caption “Correlation Matrix Heatmap Pyramid” add a markdown below it and insert the following html code:

```html
<p class="_jnb_caption">Correlation Matrix Heatmap Pyramid</p>
```

![Logo](media/image1.png)

`_jnb_caption` is the style that will be used in the report to for Microsoft Word to format the figure captions and generate the Table of Figures. Do not prefix any caption in your Jupiter notebook with figure numbers or a figure label. Microsoft Word will be responsible for automatically generating the Figure label and number. If you wish to refer to a table or Jupyter cell like a figure add a caption.

If you want to refer to blocks of code or a table output in a different TOC: Table of Figures/Tables/Code Blocks use the following reference:

| &nbsp;     | CSS class name | Html Example                                                         |
|------------|----------------|----------------------------------------------------------------------|
| Figures    | `_jnb_caption` | `<p class="_jnb_caption">Correlation Matrix Heatmap Pyramid</p>`     |
| Tables     | `_jnb_table`   | `<p class="_jnb_table">Births top 5 rows</p>`                        |
| Code Block | `_jnb_code`    | `<p class="_jnb_code"> display_jupyter_notebook_header function</p>` |
