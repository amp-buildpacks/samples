# Move on Aptos Sample

## Preparing

> Update address in `Move.toml`

```toml
[addresses]
hello_blockchain='<YOUR-ACCOUNT>'
```

## Building

```bash
pack build aptos-sample --buildpack amp-buildpacks/aptos
```

## Running

```bash
docker run -u 1001:cnb --it aptos-sample
```

## Credits

Sample codes copied from https://github.com/aptos-labs/aptos-core/tree/main/aptos-move/move-examples/my_first_dapp/move
