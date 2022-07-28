# @dhealth/paper-wallet

[![License](https://img.shields.io/badge/License-LGPL%203.0%20only-blue.svg)][license]
[![Discord](https://img.shields.io/badge/chat-on%20discord-green.svg)][discord]

dHealth paper wallet generator for [dHealth Network][parent-url].

- [Install notes](#install-notes)
- [Getting help](#getting-help)
- [Contributing](#contributing)
- [License](#license)

**NOTE**: The author(s) and contributor(s) of this package cannot be held responsible for any loss of money or for any malintentioned usage forms of this package. Please use this package with caution.

## Install notes

To install the npm module on your typescript or node project run:

`npm install @dhealth/paper-wallet --save`

And install plugin dependencies:

`npm install dhealth-sdk @dhealth/hd-wallets --save`

## Usage <a name="usage"></a>

Prepare some constants for use the module:

```javascript
import { dHealthPaperWallet } from '@dhealth/paper-wallet';

const hdRootAccount = {
    mnemonic: "guess welcome coconut forum cricket unfold welcome still ticket cluster buddy fan decrease cotton model drive student assault cloth protect random equal this congress",
    rootAccountPublicKey: "TC6B74-FLJ5MR-PSXPEM-WDBWX5-VDIXA5-L5UI36-MEA",
    rootAccountAddress: "1F032B727E910D69F1B6A3244AD1B065547AA0055BC41CF4285F662182DCC18A"
};

const privateKeyAccount = {
    name: "My private key account",
    address: "TCHBDE-NCLKEB-ILBPWP-3JPB2X-NY64OE-7PYHHE-32I",
    publicKey: "3B6A27BCCEB6A42D62A3A8D02A6F0D73653215771DE243A63AC048A18B59DA29",
    privateKey: "0000000000000000000000000000000000000000000000000000000000000000"
};

const paperWallet = new dHealthPaperWallet(hdRootAccount, [privateKeyAccount], NetworkType.TEST_NET, '57F7DA205008026C776CB6AED843393F04CD458E0AA2D9F1D5F31A402072B2D6')

const uint8Array = await paperWallet.toPdf();

```

## Getting help

Use the following available resources to get help:

- [dHealth Documentation][docs]
- Join the community on [Discord][discord]
- If you found a bug, [open a new issue][issues]

## Contributing

Contributions are welcome and appreciated.
Check [CONTRIBUTING](CONTRIBUTING.md) for information on how to contribute.

## License

Copyright 2019 Peersyst Technology SL

Licensed under the [MIT](LICENSE)

[license]: https://opensource.org/licenses/LGPL-3.0
[parent-url]: https://dhealth.com
[docs]: https://docs.dhealth.com
[issues]: https://github.com/dhealthproject/dhealth-paper-wallet/issues
[discord]: https://discord.gg/P57WHbmZjk
