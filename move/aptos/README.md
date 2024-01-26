# Move on Aptos Sample

## Preparing

> Update address in `Move.toml`

```toml
[addresses]
todolist_addr='<YOUR_ADDRESS>'
```

## Building

```bash
pack build aptos-sample --buildpack amp-buildpacks/aptos
```

## Running

```bash
docker run --it aptos-sample
```

## Credits

Sample codes copied from https://github.com/aptos-labs/aptos-core/tree/main/aptos-move/move-examples/my_first_dapp/move
