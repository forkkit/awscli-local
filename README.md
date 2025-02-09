# LocalStack AWS CLI

This package provides the `awslocal` command, which is a thin wrapper around the `aws`
command line interface for use with [LocalStack](https://github.com/localstack/localstack).

## Installation

You can install the `awslocal` command via `pip`:

```
pip install awscli-local
```

## Usage

The `awslocal` command has the same usage as the `aws` command. For detailed usage,
please refer to the man pages of `aws help`.

## Example

Instead of the following command ...

```
aws --endpoint-url=http://localhost:4568 kinesis list-streams
```

... you can simply use this:

```
awslocal kinesis list-streams
```

## Configurations

You can use the following environment variables for configuration:

* `LOCALSTACK_HOST`: Set the hostname for the localstack instance. Useful when you have
localstack is bound to another interface (i.e. docker-machine).
* `USE_SSL`: Whether to use `https` endpoint URLs (required if LocalStack has been started
with `USE_SSL=true` enabled). Defaults to `false`.

## Change Log

* v0.5: Support piping binary files to stdout; add .bat file for Windows
* v0.4: Minor fix for Python 3 compatibility
* v0.3: Add support for additional service endpoints
* v0.2: Enable SSL connections; refactor code
* v0.1: Initial release

## License

This software library is released under the Apache License, Version 2.0 (see `LICENSE`).
