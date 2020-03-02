# Instructions

In this exercise you'll be processing log-lines.

Each log line is a string formatted as follows: `"[<LEVEL>]: <MESSAGE>"`.

There are three different log levels:

- `INFO`
- `WARNING`
- `ERROR`

You have three tasks.

### 1. Parse log level

Define a `LogLevel` enum that has three elements:

- `Info`
- `Warning`
- `Error`

Next, implement a method to parse the log level of a log line:

```rust
parse_log_level("[INFO]: File deleted");
// Returns: LogLevel::Info
```

### 2. Support unknown log level

Unfortunately, occasionally some log lines have an unknown log level. To gracefully handle these log lines, add an `Unknown` member to the `LogLevel` enum which should be returned when parsing an unknown log level:

```rust
LogLine.ParseLogLevel("[FATAL]: Invalid operation")
parse_log_level("[FATAL]: File deleted");
// Returns: LogLevel::Unknown
```
