# Introduction

This is a `.clang-format` file that attempts to implement the [Barr Group's formatting standards for embedded C](https://barrgroup.com/embedded-systems/books/embedded-c-coding-standard) via the [`clang-format`](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) tool.

# Known Issues:

1. Align trailing comments doesn't always work on multi-line top-level function definitions
2. [Pre-processor indentation affects nearby comment spacing](https://github.com/petertorelli/clang-format-barr-c/issues/2)
