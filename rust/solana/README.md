# Rust on Solana Sample (native)

## Building

```
pack build solana-native-sample \
    --buildpack docker.io/paketocommunity/rust \
    --buildpack ghcr.io/amp-buildpacks/solana
```

## Running

```
docker run --interactive --tty --init solana-native-sample
```

## Credits

Sample codes copied from https://github.com/solana-developers/program-examples/tree/main/basics/hello-solana/native
