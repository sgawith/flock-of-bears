# Grep basics
To find an occurrence of a string in the current folder:

`grep -n "my string" *`

The -n switch includes the line number in the output, which is nice.

To find an occurrence of a string in the current folders and all sub-folders:

`grep -nr "my string" *`

You could also use the -i flag to make the search case-insensitive, and the search term can be a regex, which makes it powerful.

#grep #linux