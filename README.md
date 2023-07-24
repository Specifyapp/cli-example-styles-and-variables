# Specify Example - Pulling Design Tokens from Figma Styles and Figma Variables

This repository shows an example on how to work with both Figma Styles and Variables in the same GitHub repository.

## Prerequisites

- Node installed
- Specify Personal Access Token
- Specify repositories with Figma Styles synced
- Specify repositories with Figma Variables synced

## How to use

1. Clone this repository
2. Run `npm install` or `yarn install`
3. Update the `.specifyrc/configuration-with-styles.json` file with your Specify Personal Access Token and Specify repository
4. Update the `.specifyrc/configuration-with-variables.json` file with your Specify Personal Access Token and Specify repository
5. Run `npm run extract-tokens` or `yarn extract-tokens`

## How it works

The script executes the following steps:

- Executes the `specify pull` command to pull the Figma Styles by using the command `extract-tokens-with-styles`
- Executes the `specify pull` command to pull the Figma Variables by using the command `extract-tokens-with-variables`

Both of those command uses the `-C` (or `--config-path`) flag to specify which config file they should use.

The script will first pull the Figma Styles and Variables from the specified repositories. It will then extract the tokens from the Figma Styles and Variables and write them to the `output` folder. The tokens are written to the `output` folder in the following format:

```
output
├── colors
│   ├── with-styles.css
│   ├── with-variables.css
├── texts
│   ├── text-styles.css
```

## Please note

Currently the parsers for Figma Variables does not have any options contrary to the parsers for Styles. Do not hesitate to give us any feedback you deem necessary.

If you have any feedback or questions, please let us know by sending an email at [support@specifyapp.com](mailto:support@specifyapp.com)
