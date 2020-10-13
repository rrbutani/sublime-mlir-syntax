# An MLIR .sublime-syntax

## Sources
The textmate reference grammar [comes from upstream](https://github.com/llvm/llvm-project/tree/b9fa45864dea7073dbc1e39649d72b1ddadd0217/mlir/utils/textmate). This is also the grammar that GitHub (as in, [`linguist`](https://github.com/github/linguist)) [uses for MLIR code](https://github.com/github/linguist/pull/4610) (though it [lives outside](https://github.com/jpienaar/mlir-grammar) of llvm/llvm-project it appears to be, as of this writing, identical).

This grammar also draws from [the grammar](https://github.com/mlir-visualizer/mlir-vscode/blob/master/syntaxes/mlir.json) bundled with [`mlir-vscode`](https://github.com/mlir-visualizer/mlir-vscode); available separately in [this repo](https://github.com/mlir-visualizer/mlir-grammar). As [this README](https://github.com/mlir-visualizer/mlir-vscode#features) notes this grammar has specific support for several MLIR dialects.

## Misc
Docs for the sublime-syntax format are [here](http://www.sublimetext.com/docs/3/syntax.html).
Names of the scopes are available [here](https://www.sublimetext.com/docs/3/scope_naming.html).

The real reason this exists is for use with [`bat`](https://github.com/sharkdp/bat) which uses [`syntect`](https://github.com/trishume/syntect/)(meaning grammars used with it have to be in sublime-syntax form) and [supports external language definitions](https://github.com/sharkdp/bat#adding-new-syntaxes--language-definitions).
