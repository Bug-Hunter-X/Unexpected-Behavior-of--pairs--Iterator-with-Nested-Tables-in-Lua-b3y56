# Lua pairs Iterator Unexpected Behavior with Nested Tables

This repository demonstrates a potential issue with Lua's `pairs` iterator when working with deeply nested tables. The issue arises from modifying a table during iteration, leading to skipped elements or unexpected results.

## Bug Description
The provided Lua code defines a recursive function `foo` that iterates over a nested table using `pairs`.  If the table is modified within the loop, the iterator may behave unexpectedly.

## Solution
The solution involves creating a copy of the table before iteration to avoid modification during the traversal.  This ensures that the iterator works correctly and all elements are processed.