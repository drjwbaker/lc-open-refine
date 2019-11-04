---
title: "Introduction to Transformations"
teaching: 5
exercises: 5
questions:
- "How do I use transformations to programmatically edit my data?"
- "What are the kind of transformations Open Refine supports?"
- "What is GREL?"
objectives:
- "Introduce common transformations"
- "Introduce GREL, the General Refine Expression Language"
keypoints:
- "Common transformations are available through the Menu option"
---

## Introducing Transformations

Through facets, filters and clusters OpenRefine offers relatively straightforward ways of getting an overview of your data, and making changes where you want to standardise terms used to a common set of values.

However, sometimes there will be changes you want to make to the data that cannot be achieved in this way. Such types of changes include:

* Splitting data that is in a single column into multiple columns (e.g. splitting an address into multiple parts)
* Standardising the format of data in a column without changing the values (e.g. removing punctuation or standardising a date format)

To support this type of activity OpenRefine supports 'Transformations' which are ways of manipulating data in columns. Transformations are normally written in a special language called 'GREL' (General Refine Expression Language). To some extent GREL expressions are similar to Excel Formula, although they tend to focus on text manipulations rather than numeric functions.

Full documentation for the GREL is available at [https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language](https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language). This tutorial covers only a small subset of the commands available.

### Common transformations
Some transformations are used regularly and are accessible directly through menu options, without having to type them directly.

Examples of some of these common transformations are given in the table below, with their 'GREL' equivalents. We'll see how to use the GREL version later in this lesson.

Common Transformation  | Action | GREL expression
--------------------| ------------- | -------------
To Uppercase| Converts the current value to uppercase | ```value.toUppercase()```
To Lowercase| Converts the current value to lowercase | ```value.toLowercase()```
To Titlecase| Converts the current value to titlecase (i.e. each word starts with an uppercase character and all other characters are converted to lowercase) | ```value.toTitlecase()```
Trim leading and trailing whitespace | Removes any 'whitespace' characters (e.g. spaces, tabs) from the start or end of the current value | ```value.trim()```

>## Correct Date data
>1. On the date column use the dropdown menu to select ```Edit cells->Common transforms->Trim leading and trailing whitespace```
>2. A number of rows are changed. How might this have changed the quality of our previous counts of the data?
{: .checklist}
