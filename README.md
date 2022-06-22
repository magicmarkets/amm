# Token Swap AMM

Fork of
[ironaddicteddog/anchor-amm](https://github.com/ironaddicteddog/anchor-amm)
which itself is a fork of the [Solana SPL token-swap
program](https://github.com/solana-labs/solana-program-library/tree/master/token-swap)
implemented in [coral-xyz/anchor](https://github.com/coral-xyz/anchor). We're
using the anchor version as it is easier to reason about.

## Build, Deploy and Test

First, install dependencies:

```
$ yarn
```

Next, we will build and deploy the program via Anchor.

Get the program ID:

```
$ anchor keys list
anchor_amm: 4CkSf34hTH2rGmgFDCm5WCFE8sHpfdBzrBChEScJBxoM
```

Here, make sure you update your program ID in `Anchor.toml` and `lib.rs`.

Build the program:

```
$ anchor build
```

Let's deploy the program. Notice that `anchor-amm` will be deployed on a [mainnet-fork](https://github.com/DappioWonderland/solana) test validator run by Dappio:

```
$ anchor deploy
...

Program Id: 4CkSf34hTH2rGmgFDCm5WCFE8sHpfdBzrBChEScJBxoM

Deploy success
```

Finally, run the test:

```
$ anchor test --skip-build --skip-deploy
```
