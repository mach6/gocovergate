# gocovergate

`gocovergate` is a simple tool that acts as a code coverage quality gate.

It expects a coverage profile out file (default `cover.out`) to be present in the current directory.

When executed, it will print the total code coverage.
If it is below the desired-coverage (default 80), it will exit with a status code of 1.

## Installation

```text
go install github.com/mach6/gocovergate@main
```

## Usage

Run with default settings.

```shell
$ go test ./... --coverprofile cover.out
$ gocovergate
```

Run with desired coverage and non-default `coverage.out` file.

```shell
$ go test ./... --coverprofile coverage.out
$ gocovergate -cover-file coverage.out -desired-coverage 70 
```

## License
[MIT](LICENSE)
