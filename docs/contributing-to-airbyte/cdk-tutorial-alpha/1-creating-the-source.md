# Step 1: Creating the Source

Airbyte provides a code generator which bootstraps the scaffolding for our connector.

```bash
$ cd airbyte-integrations/connector-templates/generator # assumes you are starting from the root of the Airbyte project.
# Install NPM from https://www.npmjs.com/get-npm if you don't have it
$ npm install
$ npm run generate
```

Select the `Python HTTP API Source` template and then input the name of your connector. For this walk-through we will refer to our source as `python-http-example`. The finalized source code for this tutorial can be found [here](https://github.com/airbytehq/airbyte/tree/master/airbyte-integrations/connectors/source-python-http-tutorial).

The source we will build in this tutorial will pull data from the [Rates API](https://github.com/airbytehq/airbyte/tree/d940c78307f09f38198e50e54195052d762af944/docs/contributing-to-airbyte/tutorials/cdk-tutorial-alpha/ratesapi.io), a free and open API which documents historical exchange rates for fiat currencies.

