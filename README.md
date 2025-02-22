# Lua pairs iterator skips elements in nested tables with out-of-order keys

This repository demonstrates a subtle bug in Lua's `pairs` iterator.  Under specific conditions involving nested tables with keys that aren't in strictly ascending order, `pairs` can skip elements.  This is not a common problem, but it can be very difficult to debug when encountered.

The `bug.lua` file contains code that reproduces the issue. The `bugSolution.lua` file demonstrates a workaround using `ipairs` for numerical keys or a manual iteration approach.