# Safe Settings

See [.golangci.yml](.golangci.yml)

Linter that tries to follow [Uber Style Guidelines](https://github.com/uber-go/guide/blob/master/style.md)

## License

License: MIT

Source: [@ccoVeille](https://github.com/ccoVeille/golangci-lint-config-examples)

## Uber Style Guidelines

- [Guidelines](https://github.com/uber-go/guide/blob/master/style.md#guidelines)
  - [Pointers to Interfaces](https://github.com/uber-go/guide/blob/master/style.md#pointers-to-interfaces)
  - [Verify Interface Compliance](https://github.com/uber-go/guide/blob/master/style.md#verify-interface-compliance)
  - [Receivers and Interfaces](https://github.com/uber-go/guide/blob/master/style.md#receivers-and-interfaces)
  - [Zero-value Mutexes are Valid](https://github.com/uber-go/guide/blob/master/style.md#zero-value-mutexes-are-valid)
  - [Copy Slices and Maps at Boundaries](https://github.com/uber-go/guide/blob/master/style.md#copy-slices-and-maps-at-boundaries)
  - [Defer to Clean Up](https://github.com/uber-go/guide/blob/master/style.md#defer-to-clean-up)
  - [Channel Size is One or None](https://github.com/uber-go/guide/blob/master/style.md#channel-size-is-one-or-none)
  - [Start Enums at One](https://github.com/uber-go/guide/blob/master/style.md#start-enums-at-one)
  - [Use `"time"` to handle time](https://github.com/uber-go/guide/blob/master/style.md#use-time-to-handle-time)
  - [Errors](https://github.com/uber-go/guide/blob/master/style.md#errors)
    - [Error Types](https://github.com/uber-go/guide/blob/master/style.md#error-types)
    - [x] [Error Wrapping](https://github.com/uber-go/guide/blob/master/style.md#error-wrapping) - Sytle applied through `errorlint`.
    - [x] [Error Naming](https://github.com/uber-go/guide/blob/master/style.md#error-naming) - Style applied through `errname`.
    - [Handle Errors Once](#handle-errors-once)
  - [Handle Type Assertion Failures](#handle-type-assertion-failures)
  - [x] [Don't Panic](https://github.com/uber-go/guide/blob/master/style.md#dont-panic) - Style applied through `forbidigo`.
  - [Use go.uber.org/atomic](https://github.com/uber-go/guide/blob/master/style.md#use-gouberorgatomic)
  - [Avoid Mutable Globals](https://github.com/uber-go/guide/blob/master/style.md#avoid-mutable-globals)
  - [Avoid Embedding Types in Public Structs](https://github.com/uber-go/guide/blob/master/style.md#avoid-embedding-types-in-public-structs)
  - [Avoid Using Built-In Names](https://github.com/uber-go/guide/blob/master/style.md#avoid-using-built-in-names)
  - [x] [Avoid `init()`](https://github.com/uber-go/guide/blob/master/style.md#avoid-init) - Style applied through `gochecknoinits`.
  - [x] [Exit in Main](https://github.com/uber-go/guide/blob/master/style.md#exit-in-main) - Style applied through `revive.deep-exit`.
  - [x] [Use field tags in marshaled structs](https://github.com/uber-go/guide/blob/master/style.md#use-field-tags-in-marshaled-structs) - Style applied through `musttag`.
  - [Don't fire-and-forget goroutines](https://github.com/uber-go/guide/blob/master/style.md#dont-fire-and-forget-goroutines)
    - [Wait for goroutines to exit](https://github.com/uber-go/guide/blob/master/style.md#wait-for-goroutines-to-exit)
    - [No goroutines in `init()`](https://github.com/uber-go/guide/blob/master/style.md#no-goroutines-in-init)
- [Performance](https://github.com/uber-go/guide/blob/master/style.md#performance)
  - [x] [Prefer strconv over fmt](https://github.com/uber-go/guide/blob/master/style.md#prefer-strconv-over-fmt) - Style applied through `perfsprint.string-format`.
  - [Avoid repeated string-to-byte conversions](https://github.com/uber-go/guide/blob/master/style.md#avoid-repeated-string-to-byte-conversions)
  - [Prefer Specifying Container Capacity](https://github.com/uber-go/guide/blob/master/style.md#prefer-specifying-container-capacity)
- [Style](https://github.com/uber-go/guide/blob/master/style.md#style)
  - [x] [Avoid overly long lines](https://github.com/uber-go/guide/blob/master/style.md#avoid-overly-long-lines) - Style applied through `lll`.
  - [Be Consistent](https://github.com/uber-go/guide/blob/master/style.md#be-consistent)
  - [Group Similar Declarations](https://github.com/uber-go/guide/blob/master/style.md#group-similar-declarations)
  - [Import Group Ordering](https://github.com/uber-go/guide/blob/master/style.md#import-group-ordering)
  - [x] [Package Names](https://github.com/uber-go/guide/blob/master/style.md#package-names) - Style applied through linter `revive.var-naming`.
  - [x] [Function Names](https://github.com/uber-go/guide/blob/master/style.md#function-names) - Style applied through linter `revive.var-naming`.
  - [Import Aliasing](https://github.com/uber-go/guide/blob/master/style.md#import-aliasing)
  - [x] [Function Grouping and Ordering](https://github.com/uber-go/guide/blob/master/style.md#function-grouping-and-ordering) - Style applied through linter `funcorder`.
  - [x] [Reduce Nesting](https://github.com/uber-go/guide/blob/master/style.md#reduce-nesting) - Style applied through `nestif`.
  - [x] [Unnecessary Else](https://github.com/uber-go/guide/blob/master/style.md#unnecessary-else) - Style applied through `revive.superfluous-else`.
  - [Top-level Variable Declarations](https://github.com/uber-go/guide/blob/master/style.md#top-level-variable-declarations)
  - [Prefix Unexported Globals with _](https://github.com/uber-go/guide/blob/master/style.md#prefix-unexported-globals-with-_)
  - [Embedding in Structs](https://github.com/uber-go/guide/blob/master/style.md#embedding-in-structs)
  - [Local Variable Declarations](https://github.com/uber-go/guide/blob/master/style.md#local-variable-declarations)
  - [nil is a valid slice](https://github.com/uber-go/guide/blob/master/style.md#nil-is-a-valid-slice)
  - [Reduce Scope of Variables](https://github.com/uber-go/guide/blob/master/style.md#reduce-scope-of-variables)
  - [Avoid Naked Parameters](https://github.com/uber-go/guide/blob/master/style.md#avoid-naked-parameters)
  - [Use Raw String Literals to Avoid Escaping](https://github.com/uber-go/guide/blob/master/style.md#use-raw-string-literals-to-avoid-escaping)
  - [Initializing Structs](https://github.com/uber-go/guide/blob/master/style.md#initializing-structs)
    - [Use Field Names to Initialize Structs](https://github.com/uber-go/guide/blob/master/style.md#use-field-names-to-initialize-structs)
    - [Omit Zero Value Fields in Structs](https://github.com/uber-go/guide/blob/master/style.md#omit-zero-value-fields-in-structs)
    - [Use `var` for Zero Value Structs](https://github.com/uber-go/guide/blob/master/style.md#use-var-for-zero-value-structs)
    - [Initializing Struct References](https://github.com/uber-go/guide/blob/master/style.md#initializing-struct-references)
  - [x] [Initializing Maps](https://github.com/uber-go/guide/blob/master/style.md#initializing-maps) - Style applied through `revive.enforce-slice-style`.
  - [Format Strings outside Printf](https://github.com/uber-go/guide/blob/master/style.md#format-strings-outside-printf)
  - [Naming Printf-style Functions](https://github.com/uber-go/guide/blob/master/style.md#naming-printf-style-functions)
- [Patterns](https://github.com/uber-go/guide/blob/master/style.md#patterns)
  - [Test Tables](https://github.com/uber-go/guide/blob/master/style.md#test-tables)
  - [Functional Options](https://github.com/uber-go/guide/blob/master/style.md#functional-options)
- [Linting](https://github.com/uber-go/guide/blob/master/style.md#linting)
