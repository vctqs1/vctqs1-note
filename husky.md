# Something about Husky

## Husky and tropic of cancer Version 5
When you're trying to using githook and husky, having some different between verrsion <5 and >=5
1. How to add Husky into your repo, where we should put it in.
- Version <5
Add into `package.json` something like
```json
"husky": {
    "hooks": {
        "pre-commit": "lint-staged && yarn test:unit-ci" -> your script at here
    }
},
```
- Verion >=5 


3. How to trigger your Githook and Husky together
