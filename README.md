# Vulnerability cost for Snyk

## Building vsix

Directions on [Visual Studio site](https://code.visualstudio.com/api/working-with-extensions/publishing-extension), but in short:

- `npm install -g vsce`
- `vsce package`

This will run npm scripts: `check` (eslint + prettier) and `webpack` (dist files) if either fail, `vsce` doesn't report what failed so you will need to re-run these checks manually. Otherwise it will generate a (zip) `.vsix` file that can be manually installed using `code --install-extension vscode-vuln-cost-1.0.0.vsix`
