# Introduction

This is a `.clang-format` file that attempts to implement the [Barr Group's formatting standards for embedded C](https://barrgroup.com/embedded-systems/books/embedded-c-coding-standard) via the [`clang-format`](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) tool.

Issues:

1. Space before parantheses should only happen during declaration and not call instances, there is no provision for this.
2. Align trailing comments doesn't always work on multi-line top-level function definitions
3. Pre-processor indentation affects nearby comment spacing
4. ~~There's no provision for aligning consecutive variable declarations for pointers (i.e., no space after the `*` but still aligned text excluding the `*`).~~ `clang-format` v14 now right-aligns pointers correctly.

