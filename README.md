# cz-commit-emoji

> Commitizen adapter formatting commit messages using emojis.

**cz-commit-emoji** allows you to easily use emojis in your commits using [commitizen].

```sh
? Select the type of change you are committing: (Use arrow keys)
❯ feature   🌟  A new feature
  fix       🐞  A bug fix
  docs      📚  Documentation change
  refactor  🎨  A code refactoring change
  chore     🔩  A chore change
```

## Install

```bash
yarn add commitizen cz-commit-emoji --dev
```

## Usage

In `package.json`
```json
{
  ...
  "config": {
    "commitizen": {
      "path": "cz-commit-emoji"
    }
  }
}
```
or with a config file named `.czrc.js`
```bash
echo '{ "path": "cz-commit-emoji" }' > ./.czrc
```

```sh
$ git cz
```

### Types

An [Inquirer.js] choices array:

```json
{
  "config": {
    "cz-commit-emoji": {
      "types": [
        {
          "emoji": "🌟",
          "code": ":star2:",
          "description": "A new feature",
          "name": "feature"
        }
      ]
    }
  }
}
```

The value `property` must be the emoji itself.

### Scopes

An [Inquirer.js] choices array:

```json
{
  "config": {
    "cz-commit-emoji": {
      "scopes": ["home", "accounts", "ci"]
    }
  }
}
```

## Examples

- https://github.com/BarryYan/nsp

## License

MIT
