---
title: "Transforming Strings, Numbers, Dates and Booleans"
teaching: 5
exercises: 15
questions:
- "How do I use transformations to programmatically edit my data?"
- "How do I transform the various data types?"
objectives:
- "Introduce data formats"
- "Introduce Boolean values and how to run transformations based on them"
keypoints:
- "You can alter data in OpenRefine based on specific instructions"
- "You can expand the data editing functions that are built-in into OpenRefine by building your own"
---

## Data types
Understanding data types and regular expressions will help you write more complex transformations using GREL.

>## Data types in OpenRefine
>Every piece of data in OpenRefine has a 'type'. The most common 'type' is a 'string' - that is a piece of text. However there are other data types available and transformations let you convert data from one type to another where appropriate. The data types supported are:
>
>* String
>* Number
>* Date
>* Boolean
>* Array (covered in the next lesson)
{: .callout}

### Dates and Numbers
So far we've been looking only at 'String' type data. Much of the time it is possible to treat numbers and dates as strings. For example in the Date column we have the date of publication represented as a String. However, some operations and transformations only work on 'number' or 'date' type operations. The simplest example is sorting values in numeric or date order. To carry out these functions we need to convert the values to a date or number first.

>## Reformat the Date
>1. Make sure you remove all Facets and Filters
>2. On the Date column use the dropdown menu to select ```Edit cells->Common transforms->To date```
>3. Note how the values are now displayed in green and follow a standard convention for their display format (ISO 8601) - this indicates they are now stored as date data types in OpenRefine. We can now carry out functions that are specific to Dates
>4. On the Date column dropdown select ```Edit column->Add column based on this column```. Using this function you can create a new column, while preserving the old column
>5. In the 'New column name' type "Formatted Date"
>6. In the 'Expression' box type the GREL expression ```value.toString("dd MMMM yyyy")```
{: .checklist}
