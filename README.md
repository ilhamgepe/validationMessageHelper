# Validation Message Helper

The `validationMessageHelper` package provides utility functions to handle validation errors returned by the Go Playground's validator library. It simplifies the process of generating descriptive error messages for validation failures.

## Features

- Easily convert validation errors into a map of field-specific error messages.
- Support for common validation tags such as `email`, `required`, `min`, and `max`.
- Customizable error messages to suit your application's needs.

## Installation

You can install the package using `go get`:

```bash
go get github.com/ilhamgepe/validationMessageHelper
```

## Usage

```go
package main

import (
	"fmt"
	"github.com/ilhamgepe/validationMessageHelper"
)

func main() {
	// Example usage
	err := validate.Struct(mystruct)
	if err != nil {
		errors := validationMessageHelper.GenerateMessage(err)
		fmt.Println(errors)
        // or return as a response
        // since GenerateMessage() only return map[string]string
	}
}

```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or create a pull request.

## License

This package is licensed under the [MIT License](LICENSE).
