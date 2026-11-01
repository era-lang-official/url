# Era URL (`github.com/era-lang-official/url`)

RFC 3986 URL parsing, serialization, and query parameter handling for Era.

## Features
- **Parsing**: `parse_url` handles schemes, host, port, path, query, and fragments.
- **Query Params**: Parameter encoding, decoding, and extraction.
- **Component Encoding**: `encode_uri_component` and `decode_uri_component`.

## Usage
```era
import "github.com/era-lang-official/url";

fn main() {
    let u = parse_url("https://api.era.org:8443/v1/users?page=2#top".to_string()).unwrap();
    println(u.host); // "api.era.org"
    println(u.get_param("page".to_string()).unwrap()); // "2"
}
```

