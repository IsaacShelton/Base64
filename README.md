# Base64
Base64 encoding/decoding library for Adept

### Easy download

Ensure your Adept compiler supports version `2.5`

```
cd <project folder>
adept install base64
```

### API

- `func base64\decode(input String) String`
- `func base64\decode(input String, output *String) successful`
- `func base64\decode(src *ubyte, len usize, out_len *usize) *ubyte`
  - *Returns `null` on error*
- `func base64\encode(input String) String`
- `func base64\encode(input String, output *String, do_newlines bool = false) successful`
- `func base64\encode(src *ubyte, len usize, out_len *usize, do_newlines bool = false) *ubyte`
  - *Returns `null` on error*

### Usage Example

```
import basics
import "base64/base64.adept"

func main {
    message String = "Hello World"
    encoded String = base64\encode(message)

    printf("Original Message: \t%S\n", message)
    printf("Encoded  Message: \t%S\n", encoded)
    printf("Decoded  Message: \t%S\n", base64\decode(encoded))
}
```

