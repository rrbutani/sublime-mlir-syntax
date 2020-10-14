# An MLIR .sublime-syntax grammar

## Sources
The textmate reference grammar [comes from upstream](https://github.com/llvm/llvm-project/tree/b9fa45864dea7073dbc1e39649d72b1ddadd0217/mlir/utils/textmate). This is also the grammar that GitHub (as in, [`linguist`](https://github.com/github/linguist)) [uses for MLIR code](https://github.com/github/linguist/pull/4610) (though it [lives outside](https://github.com/jpienaar/mlir-grammar) of `llvm/llvm-project` it appears to be — as of this writing — identical).

This grammar also draws from [the grammar](https://github.com/mlir-visualizer/mlir-vscode/blob/master/syntaxes/mlir.json) bundled with [`mlir-vscode`](https://github.com/mlir-visualizer/mlir-vscode); available separately in [this repo](https://github.com/mlir-visualizer/mlir-grammar). As [this README](https://github.com/mlir-visualizer/mlir-vscode#features) notes that grammar has specific support for several MLIR dialects.

## Misc
Docs for the `sublime-syntax` format are [here](http://www.sublimetext.com/docs/3/syntax.html).
Names of the scopes are available [here](https://www.sublimetext.com/docs/3/scope_naming.html).

The real reason this exists is for use with [`bat`](https://github.com/sharkdp/bat) which uses [`syntect`](https://github.com/trishume/syntect/) (meaning grammars used with it have to be in `sublime-syntax` form) and [supports external language definitions](https://github.com/sharkdp/bat#adding-new-syntaxes--language-definitions).

## Installation

### For use with `bat`

```bash
# Download it to the right dir:
mkdir -p "$(bat --config-dir)/syntaxes"
curl -Ls https://raw.githubusercontent.com/rrbutani/sublime-mlir-syntax/main/mlir.sublime-syntax > "$(bat --config-dir)/syntaxes/mlir.sublime-syntax"

# Get `bat` to pick it up:
bat cache --build

# Test it out:
curl -Ls https://raw.githubusercontent.com/rrbutani/sublime-mlir-syntax/main/sample.mlir | bat -lmlir
```

### For use with Sublime Text

(TODO! make a package, link to it here and in the repo's tagline)
