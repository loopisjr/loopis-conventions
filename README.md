# Loopis Conventions

## Começando
```sh
# Instale a cli do commitlint
npm install @commitlint/cli --save-dev

# Instale as regras da loopis
npm install loopis-conventions --save-dev

# Configure commitlint para usar as configurações da loopis
echo "module.exports = {extends: ['./node_modules/loopis-conventions']};" > commitlint.config.js

# Instale o husky
npm install husky --save-dev
```

Depois disso adicione ao seu `package.json` o código a baixo:

```json
{
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  }
}
```
