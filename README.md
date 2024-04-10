# Typescript Eslint minimal demo

Using nodejs v20.11.1 on Linux.

This produces no output - lints no file. Why?

```
npm i
npx eslint@8
```

This produces error even that we have `eslint.config.mjs` in ignores:

```
npm i
npx eslint@9
```

```
Oops! Something went wrong! :(

ESLint: 9.0.0

Error: Error while loading rule '@typescript-eslint/await-thenable': You have used a rule which requires parserServices to be generated. You must therefore provide a value for the "parserOptions.project" property for @typescript-eslint/parser.
Parser: undefined
Note: detected a parser other than @typescript-eslint/parser. Make sure the parser is configured to forward "parserOptions.project" to @typescript-eslint/parser.
Occurred while linting /home/martin/maptiler/eslint-test/eslint.config.mjs
    at throwError (/home/martin/maptiler/eslint-test/node_modules/@typescript-eslint/utils/dist/eslint-utils/getParserServices.js:40:11)
    at getParserServices (/home/martin/maptiler/eslint-test/node_modules/@typescript-eslint/utils/dist/eslint-utils/getParserServices.js:26:9)
    at create (/home/martin/maptiler/eslint-test/node_modules/@typescript-eslint/eslint-plugin/dist/rules/await-thenable.js:46:55)
    at Object.create (/home/martin/maptiler/eslint-test/node_modules/@typescript-eslint/utils/dist/eslint-utils/RuleCreator.js:38:20)
    at createRuleListeners (/home/martin/.npm/_npx/a064f98759e3e66d/node_modules/eslint/lib/linter/linter.js:1003:21)
    at /home/martin/.npm/_npx/a064f98759e3e66d/node_modules/eslint/lib/linter/linter.js:1129:84
    at Array.forEach (<anonymous>)
    at runRules (/home/martin/.npm/_npx/a064f98759e3e66d/node_modules/eslint/lib/linter/linter.js:1061:34)
    at Linter._verifyWithFlatConfigArrayAndWithoutProcessors (/home/martin/.npm/_npx/a064f98759e3e66d/node_modules/eslint/lib/linter/linter.js:1910:31)
    at Linter._verifyWithFlatConfigArray (/home/martin/.npm/_npx/a064f98759e3e66d/node_modules/eslint/lib/linter/linter.js:2046:21)
```
