# Something about Husky

## Husky and boundary Version 5
When you're trying to using githook and husky, having some different between verrsion <5 and >=5
1. How to add Husky into your repo, where we should put it in.

- Version <5

Add into `package.json` something like
```json
"husky": {
    "hooks": {
        "pre-commit": "yarn lint" -> your script at here
    }
},
```
- Verion >=5

Run this script `npx husky add .husky/pre-commit 'yarn lint'` to create `pre-commit` hook
And got file `.husky/pre-commit`

![image](https://user-images.githubusercontent.com/30227910/133891375-e040c1aa-301e-45c4-b075-924ba4eca6b4.png)

You change change your script, to add any hook whatever you want
```sh
applypatch-msg 
pre-applypatch
post-applypatch
pre-commit
...
```

3. The problem, easily encountered, when using both Githook and Husky together
Something, husky doesnot work well, it donot recorgize your hook to trigger your script


Check your file `.git/config`. please notice about this variable `hooksPath = true`![image](https://user-images.githubusercontent.com/30227910/133891550-f40b42b9-353c-473f-8cf0-353af9500193.png)

- Version <5: should be removed here
- Verion >=5: should add them :)
