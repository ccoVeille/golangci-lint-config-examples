# Safe Settings

See [.golangci.yml](.golangci.yml)

Linter that tries to follow [Uber Style Guidelines](https://github.com/uber-go/guide/blob/master/style.md)

## License

License: MIT

Source: [@ccoVeille](https://github.com/ccoVeille/golangci-lint-config-examples)

## Uber Style Guidelines

- [Guidelines](https://github.com/uber-go/guide/blob/master/style.md#guidelines)
  - [Pointers to Interfaces](#pointers-to-interfaces)
  - [Verify Interface Compliance](#verify-interface-compliance)
  - [Receivers and Interfaces](#receivers-and-interfaces)
  - [Zero-value Mutexes are Valid](#zero-value-mutexes-are-valid)
  - [Copy Slices and Maps at Boundaries](#copy-slices-and-maps-at-boundaries)
  - [Defer to Clean Up](#defer-to-clean-up)
  - [Channel Size is One or None](#channel-size-is-one-or-none)
  - [Start Enums at One](#start-enums-at-one)
  - [Use `"time"` to handle time](#use-time-to-handle-time)
  - [Errors](#errors)
    - [Error Types](#error-types)
    - [Error Wrapping](#error-wrapping)
    - [x] [Error Naming](#error-naming) - Style applied through `errname`
    - [Handle Errors Once](#handle-errors-once)
  - [Handle Type Assertion Failures](#handle-type-assertion-failures)
  - [x] [Don't Panic](#dont-panic) - Style applied through `forbidigo`.
  - [Use go.uber.org/atomic](#use-gouberorgatomic)
  - [Avoid Mutable Globals](#avoid-mutable-globals)
  - [Avoid Embedding Types in Public Structs](#avoid-embedding-types-in-public-structs)
  - [Avoid Using Built-In Names](#avoid-using-built-in-names)
  - [x] [Avoid `init()`](#avoid-init) - Style applied through `gochecknoinits`.
  - [x] [Exit in Main](#exit-in-main) - Style applied through `revive.deep-exit`.
  - [Use field tags in marshaled structs](#use-field-tags-in-marshaled-structs)
  - [Don't fire-and-forget goroutines](#dont-fire-and-forget-goroutines)
    - [Wait for goroutines to exit](#wait-for-goroutines-to-exit)
    - [No goroutines in `init()`](#no-goroutines-in-init)
- [Performance](#performance)
  - [x] [Prefer strconv over fmt](#prefer-strconv-over-fmt) - Style applied through `perfsprint`
  - [Avoid repeated string-to-byte conversions](#avoid-repeated-string-to-byte-conversions)
  - [Prefer Specifying Container Capacity](#prefer-specifying-container-capacity)
- [Style](#style)
  - [x] [Avoid overly long lines](#avoid-overly-long-lines) - Style applied through `lll`
  - [Be Consistent](#be-consistent)
  - [Group Similar Declarations](#group-similar-declarations)
  - [Import Group Ordering](#import-group-ordering)
  - [Package Names](#package-names)
  - [Function Names](#function-names)
  - [Import Aliasing](#import-aliasing)
  - [x] [Function Grouping and Ordering](#function-grouping-and-ordering) - Style applied through linter `funcorder`.
  - [Reduce Nesting](#reduce-nesting)
  - [Unnecessary Else](#unnecessary-else)
  - [Top-level Variable Declarations](#top-level-variable-declarations)
  - [Prefix Unexported Globals with _](#prefix-unexported-globals-with-_)
  - [Embedding in Structs](#embedding-in-structs)
  - [Local Variable Declarations](#local-variable-declarations)
  - [nil is a valid slice](#nil-is-a-valid-slice)
  - [Reduce Scope of Variables](#reduce-scope-of-variables)
  - [Avoid Naked Parameters](#avoid-naked-parameters)
  - [Use Raw String Literals to Avoid Escaping](#use-raw-string-literals-to-avoid-escaping)
  - [Initializing Structs](#initializing-structs)
    - [Use Field Names to Initialize Structs](#use-field-names-to-initialize-structs)
    - [Omit Zero Value Fields in Structs](#omit-zero-value-fields-in-structs)
    - [Use `var` for Zero Value Structs](#use-var-for-zero-value-structs)
    - [Initializing Struct References](#initializing-struct-references)
  - [Initializing Maps](#initializing-maps)
  - [Format Strings outside Printf](#format-strings-outside-printf)
  - [Naming Printf-style Functions](#naming-printf-style-functions)
- [Patterns](#patterns)
  - [Test Tables](#test-tables)
  - [Functional Options](#functional-options)
- [Linting](#linting)
