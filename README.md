## Array-Map JSON Smartmodule

SmartModule that transforms a JSON aggregate containing arrays into individual JSON Records. This SmartModule is [array_map] type, where each record-in generates a one or more records-out.

### Expected Input

Array in JSON representation:

```json
[{"one": 1}, {"two": 2}]
```

### Expected Ouptput

Each array element is converted to individual record:

```json
{"one":1}
{"two":2}
```

## SMDK Compatible

This project works with `smdk` command tools:

```
smdk build
```

Test small file:

```
smdk test --file ./test-data/simple.json --raw
```

Test larger file and return formatted json (requires `jq`):

```
smdk test --file ./test-data/input.json --raw | jq
```

## Cargo Compatible

Build & Test

```
cargo build
```

```
cargo build
```


[array_map]: https://www.fluvio.io/smartmodules/transform/array-map/