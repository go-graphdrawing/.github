<p align="center">
  <img src="https://raw.githubusercontent.com/go-graphdrawing/brand/main/png/color/256/go-graphdrawing.png" alt="go-graphdrawing" width="88" height="88">
</p>

# go-graphdrawing

[![License](https://img.shields.io/badge/license-BSD--3--Clause-blue.svg)](https://github.com/go-graphdrawing)
[![Pure Go](https://img.shields.io/badge/pure%20Go-CGO%3D0-00ADD8?logo=go&logoColor=white)](https://github.com/go-graphdrawing)

**Placing a graph on a plane** — pure Go, CGO=0. Sugiyama layering, force-directed
placement, trees, planar embeddings.

The name is the discipline's own: *graph drawing*, as in the GD conference and
Di Battista, Eades, Tamassia and Tollis. The code is meant to read like the
literature it implements. It is deliberately **not** called `layout`, which in
this fleet already means widget layout.

## Status

**Reserved, not yet built.** The name and the shape are settled; the code waits
for a consumer that needs it.

The measurement that set that priority: the reference implementation — pgf's
`graphdrawing`, driven from LuaTeX — is **167 files and 37 163 lines of Lua**, of
which some 2 000 are TeX↔Lua glue a Go port would not need. Across a corpus of
**10 025 real beamer talks, 5 use it**. Building it for TeX would be the worst
effort-to-effect trade in that project.

The trigger will come from elsewhere: isometric and node-link **diagrams**, where
automatic placement is the feature rather than a footnote. Graph placement is not
TeX-specific, and it should not be born inside a TeX engine — the same reason
[go-typeset](https://github.com/go-typeset) exists.
