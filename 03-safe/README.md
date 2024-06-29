# Safe Settings

See [.golangci.yml](.golangci.yml)

It's [02-basic](../02-basic) plus :
- [gci](#gci)
- [thelper](#thelper)
- [mirror](#mirror)
- [usestdlibvars](#usestdlibvars)
- [dupwords](#dupwords)
- [misspell](#misspell)

## License

License: MIT

Source: [@ccoVeille](https://github.com/ccoVeille/golangci-lint-config-examples)

## Enabled linters

### errcheck
 Errcheck is a program for checking for unchecked errors in Go code.

### gosimple
 Linter for Go source code that specializes in simplifying code.

### govet
 Vet examines Go source code and reports suspicious constructs.

### ineffassign
 Detects when assignments to existing variables are not used.

### staticcheck
 It's a set of rules from staticcheck. See https://staticcheck.io/

### gci
 check imports order and makes it always deterministic.

### thelper
 make sure to use t.Helper() when needed

### mirror
 mirror suggests rewrites to avoid unnecessary []byte/string conversion

### usestdlibvars
 detect the possibility to use variables/constants from the Go standard library.

### misspell
Finds commonly misspelled English words.

### dupword
Checks for duplicate words in the source code.

### revive
 Fast, configurable, extensible, flexible, and beautiful linter for Go.
 Drop-in replacement of golint.

#### blank-imports
Blank import should be only in a main or test package, or have a comment justifying it.

#### context-as-argument
context.Context() should be the first parameter of a function when provided as argument.

#### context-keys-type
Basic types should not be used as a key in `context.WithValue`

#### dot-imports
Importing with `.` makes the programs much harder to understand

#### empty-block
Empty blocks make code less readable and could be a symptom of a bug or unfinished refactoring.

#### error-naming
for better readability, variables of type `error` must be named with the prefix `err`.

#### error-return
for better readability, the errors should be last in the list of returned values by a function.

#### error-strings
for better readability, error messages should not be capitalized or end with punctuation or a newline.

#### errorf
report when replacing `errors.New(fmt.Sprintf())` with `fmt.Errorf()` is possible

#### increment-decrement
incrementing an integer variable by 1 is recommended to be done using the `++` operator

#### indent-error-flow
highlights redundant else-blocks that can be eliminated from the code

#### range
This rule suggests a shorter way of writing ranges that do not use the second value.

#### receiver-naming
receiver names in a method should reflect the struct name (p for Person, for example)

#### redefines-builtin-id
redefining built-in names (true, false, append, make) can lead to bugs very difficult to detect.

#### superfluous-else
redundant else-blocks that can be eliminated from the code.

#### time-naming
prevent confusing name for variables when using `time` package

#### unexported-return
warns when an exported function or method returns a value of an un-exported type.

#### unreachable-code
spots and proposes to remove unreachable code. also helps to spot errors

#### unused-parameter
Functions or methods with unused parameters can be a symptom of an unfinished refactoring or a bug.

#### var-declaration
report when a variable declaration can be simplified

#### var-naming
warns when initialism, variable or package naming conventions are not followed.

## Changelog

- 2024-06-28 - golangci-lint:1.59.1

  initial version
