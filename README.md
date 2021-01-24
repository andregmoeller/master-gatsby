# Master Gatsby

This is a repository I created to accompany my viewing of [Master Gatsby](https://github.com/wesbos/master-gatsby).

## External services

### Sanity.io

This project uses [Sanity](https://www.sanity.io/) to store its data. Please go to the directory `sanity` and run:

```
npm i -g @sanity/cli
```

This will install the Sanity CLI tool. Then please run `sanity init` to initialize a new Sanity project. Thereafter log in to Sanity, open the newly created project, look up the project ID and enter the ID into the `gatsby//gatsby-config.js` and `sanity/sanity.json` files. Back on sanity.io, `http://localhost:3333`, `http://localhost:8000` and `http://localhost:8888` must be entered as values for `CORS Origins` under Settings. Finally, an API token must be generated. This token is needed for an environment variable.

#### Sample Data

The file `sanity/sample-data/all-sample-data.gz` contains test data. You can import the data by running `sanity dataset import ./sample-data/all-sample-data.gz production --replace`.

### Ethereal

[Ethereal](http://ethereal.email/) is used for testing email delivery. So, please create an account.

## Environment variables

Please go to the directory backend and rename the the file variables.env.sample to .env, open the file in an editor and enter the respective information. You will need to change the values for

- SANITY_TOKEN
- MAIL_USER
- MAIL_PASS
- GATSBY_GRAPHQL_ENDPOINT

## Starting the project on your local computer

Please go to the directory `gatsby` and run `npm run netlify` to start the project. Open http://localhost:8888 to view it in the browser.
