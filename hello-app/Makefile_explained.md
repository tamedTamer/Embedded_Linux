# Makefile Explanation

- `CC ?= gcc` → compiler is gcc unless overridden (for cross-compile).
- `CFLAGS ?= -Wall -O2` → warnings + optimization level.
- `all: hello` → default target builds hello.
- `hello: hello.c` → rule to compile hello.c into hello binary.
- `clean` → remove built binary.
