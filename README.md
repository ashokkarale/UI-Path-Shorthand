# Ui Path Shorthands useful for RPA Developer :robot:
1. LINQ Queries
  	- Filter DataTable and Select a column as a List. [Reference Q&A](https://stackoverflow.com/questions/68089211/create-a-list-of-elements-from-a-datatable-linq-column)
`dtStudent.AsEnumerable().Where(Function(row) row("First Name").ToString().StartsWith("R")).Select(Function (row) row("Last Name").ToString()).Distinct().ToList()`

  	- Filter DataTable Where a column condition and return DataTable.
`dtStudent.AsEnumerable().Where(Function (row) cint(row("No")) = 5).CopyToDataTable`

  	- Filter DataTable Where a column condition and return count of the rows returned.
`dtStudent.AsEnumerable().Where(Function (row) row("First Name").ToString.Length > 5).Count()`
