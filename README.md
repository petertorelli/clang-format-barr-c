# Config file for clang-format to implement BARR-C

This is a `.clang-format` file that attempts to implement the [Barr Group's formatting standards for embedded C](https://barrgroup.com/embedded-systems/books/embedded-c-coding-standard) via the [`clang-format`](https://clang.llvm.org/docs/ClangFormatStyleOptions.html) tool.

## Usage

1. Install clang-format in one of the following ways:
 - From package manager (e.g. `sudo apt-get install clang-format`)
 - Download the entire [LLVM toolchain](http://llvm.org/releases/) and extract the `clang-format` binary. Just extract the `.tar.xz` file and copy `bin/clang-format` into your `PATH` (e.g. `/usr/local/bin`).
2. Copy [.clang-format](.clang-format) from this repository to your local directory
3. Run `clang-format -i *.{c,h,cpp,hpp}` to format all c/c++ files in the folder
4. Optionally, you can [integrate clang-format with your IDE](https://clang.llvm.org/docs/ClangFormat.html)

## Known Issues:

1. Space before parantheses should only happen during declaration and not call instances, there is no provision for this.
2. Align trailing comments doesn't always work on multi-line top-level function definitions
3. [Pre-processor indentation affects nearby comment spacing](https://github.com/petertorelli/clang-format-barr-c/issues/2)
4. [Add InsertBraces](https://github.com/petertorelli/clang-format-barr-c/issues/4)
