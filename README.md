# Open Payments Example

This script sends money between two wallet addresses, using the [Open Payments client](https://github.com/interledger/open-payments/tree/main/packages/open-payments).

The script creates an incoming payment on the receiving wallet address, and a quote on the sending wallet address (after getting grants for both). It also creates an interactive outgoing payment grant, which will require user interaction.

The script then finalizes the grant (after it's accepted interactively via the browser), and creates the outgoing payment.

### Steps

1. Make sure you have NodeJS installed
2. Run `npm install`
3. Get a private key, client wallet address and keyId from the [test wallet](https://wallet.interledger-test.dev/), and add them in the script.
4. Pick a receiving wallet address, and a sending wallet address.
5. Run `node index.js`
6. Click on the outputted URL, to accept the outgoing payment grant.
7. Return to the terminal, hit enter. After this, the script will create the outgoing payment and funds will move between the receiver and the sender!
