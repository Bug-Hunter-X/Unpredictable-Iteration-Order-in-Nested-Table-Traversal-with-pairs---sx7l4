# Lua Nested Table Traversal Bug

This repository demonstrates a potential issue with Lua's `pairs()` iterator when used to traverse nested tables.  The `pairs()` function doesn't guarantee a specific iteration order, and modifications to the table during iteration can lead to unpredictable results.

The `bug.lua` file contains code that recursively iterates over a nested table.  Under certain conditions (especially modification during traversal), this can cause elements to be skipped or an infinite loop to occur.

The `bugSolution.lua` file provides a solution to address this by using a copy of the table, thereby preventing any iteration issues caused by table modifications during traversal.