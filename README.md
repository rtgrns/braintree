# Braintree Express Example

[![Build Status](https://github.com/braintree/braintree_express_example/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/braintree/braintree_express_example/actions/workflows/ci.yml)

An example Braintree integration for Node in the Express framework.

## Setup Instructions

1. Install packages:

   ```sh
   npm install
   ```

2. Copy the contents of `example.env` into a new file named `.env` and fill in your Braintree API credentials. Credentials can be found by navigating to Account > My User > View Authorizations in the Braintree Control Panel. Full instructions can be [found on our support site](https://articles.braintreepayments.com/control-panel/important-gateway-credentials#api-credentials).

3. Start the server:

   ```sh
   npm start
   ```

   By default, this runs the app on port `3000`. You can configure the port by setting the environmental variable `PORT`.

## Running tests

To run unit tests, use `npm run test:unit`. These do not require a server and do not make API calls.

To run all tests, run `npm test`. This requires the server be up (in a separate shell using `npm run dev` or `npm start`) to make the relevant API calls to Braintree. `npm test` requires that your _sandbox_ Braintree credentials be set up [as detailed above](#setup-instructions).

## Testing Transactions

Sandbox transactions must be made with [sample credit card numbers](https://developers.braintreepayments.com/reference/general/testing/node#credit-card-numbers), and the response of a `Transaction.sale()` call is dependent on the [amount of the transaction](https://developers.braintreepayments.com/reference/general/testing/node#test-amounts).

## Help

- Found a bug? Have a suggestion for improvement? Want to tell us we're awesome? [Submit an issue](https://github.com/braintree/braintree_express_example/issues)
- Trouble with your integration? Contact [Braintree Support](https://support.braintreepayments.com/) / support@braintreepayments.com
- Want to contribute? [Submit a pull request](https://help.github.com/articles/creating-a-pull-request)

## Disclaimer

This code is provided as is and is only intended to be used for illustration purposes. This code is not production-ready and is not meant to be used in a production environment. This repository is to be used as a tool to help merchants learn how to integrate with Braintree. Any use of this repository or any of its code in a production environment is highly discouraged.
