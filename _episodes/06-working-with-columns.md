---
title: "Working with columns and sorting"
teaching: 5
exercises: 5
questions:
- "How do I move, rename or remove columns in OpenRefine?"
- "How do I sort data in OpenRefine?"
objectives:
- "Explain how to reorder, rename and remove columns"
- "Explain how to sort data in columns"
keypoints:
- "You can reorder, rename and remove columns in OpenRefine"
- "Sorting in OpenRefine always sorts all rows"
- "The original order of rows in OpenRefine is maintained during a sort until you use the option to Reorder Rows Permanently"
---

## Reordering and renaming columns
You can re-order the columns by clicking the drop-down menu at the top of the first column (labelled 'All'), and choosing `Edit columns->Re-order / remove columns …`

You can then drag and drop column names to re-order the columns, or remove columns completely if they are not required.

Remember the incorrect values we found earlier in `Column 7`? Now seems a good time to resolve it. We're going to do this by removing data from Refine, but keeping a copy to come back to and revolve.

So, on `Column 14` do a 'facet by blank' and hit 'false'. There are 21 dodgy records which by scanning we can quickly see are muddled. Hit 'Export' to grab a local copy of these 21 records only. We can then hit the 'All' dropdown, 'edit rows', and 'Remove all matching rows' to delete these pesky records. If we reset the facet we can now start to tidy up our data, keeping only Columns 1-11 (that have meaningful data), and renaming the columns we think we understand (Description, Date).

## Sorting data
You can sort data in OpenRefine by clicking on the drop-down menu for the column you want to sort on, and choosing `Sort`.

Once you have sorted the data, a new `Sort` drop-down menu will be displayed.

Unlike in Excel, 'Sorts' in OpenRefine are temporary - that is, if you remove the `Sort`, the data will go back to its original 'unordered' state. The 'Sort' drop-down menu lets you amend the existing sort (e.g., reverse the sort order), remove existing sorts, and/or make sorts permanent.

You can sort on multiple columns at the same time by adding another sorted column (in the same way).

Doing this on our `Date` field reveals more problems we need to resolve.
