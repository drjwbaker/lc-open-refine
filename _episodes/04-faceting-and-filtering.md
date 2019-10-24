---
title: "Faceting and filtering"
teaching: 10
exercises: 10
questions:
- "What is a facet in OpenRefine?"
- "What is a filter in OpenRefine?"
- "How can I use filters and facets to explore data OpenRefine?"
- "How can I easily correct common data issues in my data with OpenRefine?"
objectives:
- "Explain what Facets and Filters are"
- "Answer questions about the content of a data set using Facets"
- "Use facets and filters to work with a subset of data"
- "Correct data problems through a facet"
keypoints:
- "You can use facets and filters to explore your data"
- "You can use facets and filters work with a subset of data in OpenRefine"
- "You can easily correct common data issues from a Facet"
---

## Facets
Facets are one of the most useful features of OpenRefine and can help both get an overview of the data in a project as well as helping you bring more consistency to the data.

A 'Facet' groups all the values that appear in a column, and then allows you to filter the data by these values and edit values across many records at the same time.

The simplest type of Facet is called a 'Text facet'. This simply groups all the text values in a column and lists each value with the number of records it appears in. The facet information always appears in the left hand panel in the OpenRefine interface.

To create a Text Facet for a column, click on the drop down menu at the top of Column 8 and choose `Facet -> Text Facet`. The facet will then appear in the left hand panel. If we are speculating that this column contains the names of photographers (which I am), we note some errors in our data to which we shall return. For the moment, hit `count` in the left hand panel to see the other use of Open Refine, that it gives you a sense of the themes in a column.

The facet consists of a list of values used in the data. You can filter the data displayed by clicking on one of these headings.

You can include multiple values from the facet in a filter at one time by using the `Include` option which appears when you put your mouse over a value in the Facet.

You can also `invert` the filter to show all records which do not match your selected values. This option appears at the top of the Facet panel when you select a value from the facet to apply as a filter.

>## Let's create a text facet
>1. Click on the drop down menu at the top of Column 8 and choose `Facet > Text Facet`. The facet will then appear in the left hand panel. Choose the to sort by `count`.
>2. To select a single value, just click the relevant line in the facet
>3. To select multiple values click the `Include` option on the appropriate line in the facet (which only appears when you mouse over the line)
>3. You can 'invert' your selections to `exclude`
>4. Include a value and then look at top to invert inclusion.
{: .checklist}

## Filters
As well as using Facets to filter the data displayed in OpenRefine you can also apply 'Text Filters' which looks for a particular piece of text appearing in a column. Text filters are applied by clicking the drop down menu at the top of the column you want to apply the filter to and choosing 'Text filter'.

As with Facets, the Filter options appear in the left hand panel in OpenRefine. Simply type in the text you want to use in the Filter - e.g. `Ellis` - to display only rows which contain that text in the relevant column.

## Working with filtered data
It is very important to note that when you have filtered the data displayed in OpenRefine, any operations you carry out will apply only to the rows that match the filter - that is the data currently being displayed.

## Other types of Facet 
As well as 'Text facets' Refine also supports a range of other types of facet. These include:

* Numeric facets
* Timeline facets (for dates)
* Custom facets
* Scatterplot facets

**Numeric and Timeline facets** display graphs instead of lists of values. The graph includes 'drag and drop' controls you can use to set a start and end range to filter the data displayed.

**Scatterplot facets** are less commonly used. For further information on these see the tutorial at [https://web.archive.org/web/20190105063215/http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial#Exploring_the_data_with_scatter_plots](https://web.archive.org/web/20190105063215/http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial#Exploring_the_data_with_scatter_plots).

**Custom facets** are a range of different types of facets. Some of the default custom facets are:

* Word facet - this breaks down text into words and counts the number of records each word appears in
* Duplicates facet - this results in a binary facet of 'true' or 'false'. Rows appear in the 'true' facet if the value in the selected column is an exact match for a value in the same column in another row
* Text length facet - creates a numeric facet based on the length (number of characters) of the text in each row for the selected column. This can be useful for spotting incorrect or unusual data in a field where specific lengths are expected (e.g. if the values are expected to be years, any row with a text length more than 4 for that column is likely to be incorrect)
* Facet by blank - a binary facet of 'true' or 'false'. Rows appear in the 'true' facet if they have no data present in that column. This is useful when looking for rows missing key data.

Facets are intended to group together common values and OpenRefine limits the number of values allowed in a single facet to ensure the software does not perform slowly or run out of memory. If you create a facet where there are many unique values (for example, a facet on a 'book title' column in a data set that has one row per book) the facet created will be very large and may either slow down the application, or OpenRefine will not create the facet.

>## Find all entries with a photographer name
>* If we accept that Column 8 lists the surnames of photographers, use the `Facet by blank` function to find all photographs in this data set without a named photographer
>
>>## Solution
>>
>>1. On `Column 8` drop down and select `Customized facets > Facet by blank`
>>2. `True` means that it is blank, so you can:
>>    * Select `include` on True in the facet to filter the list of publications to only those that don't have a DOI
>{: .solution}
{: .challenge}

## Amending data through facets
If you create a text facet you can edit the values in the facet to change the value for several records at the same time. To do this, simply mouse-over the value you want to edit and click the 'edit' option that appears.

This approach is useful in relatively small facets where you might have small variations through punctuation or typing errors etc. For example, a column that should contain only terms from a small restricted list such as days of the week or months of the year.

The list of values in the facet will update as you make edits.

>## Correct the Language values via a facet
>
>* `Text facet` on the `Column 11` and correct the variation in the `Sir Joseph Causton & Sons` and `Sir Joseph Causton & Sons Ltd` values.
>
>>## Solution
>>1. Create a Text facet on the Language column
>>2. Notice that there is both `Sir Joseph Causton & Sons` and `Sir Joseph Causton & Sons Ltd`
>>3. Put the mouse over the `Sir Joseph Causton & Sons` value
>>4. Click `Edit`
>>5. Type `Sir Joseph Causton & Sons Ltd` and click `Apply`
>>6. See how the `Column 11` facet updates
>{: .solution}
{: .challenge}
