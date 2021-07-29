# Slimsag's SublimeHQ Packages Fork

> **These packages are developed against the latest [Sublime Text 3 Dev Build](http://sublimetext.com/3dev). Bugs may exist on older builds, and the format used is not compatible with builds older than 3092.**

## Installation

If you want to make changes to these packages and test them locally, fork this repository and then symlink the changed packages into your *Packages* folder.

*Replace `Python` in the following commands with the name of the syntax to install.*

### OS X

```bash
$ git clone https://github.com/sublimehq/Packages.git
$ ln -s `pwd`/Packages/Python ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/
```

### Linux

```bash
$ git clone https://github.com/sublimehq/Packages.git
$ ln -s `pwd`/Packages/Python ~/.config/sublime-text-3/Packages/
```

### Windows

On Windows, you can use directory junctions instead of symlinks (symlinks require administrative rights; directory junctions don't):

```powershell
# Using PowerShell
PS> git clone https://github.com/sublimehq/Packages.git
PS> cmd /c mklink /J "$env:APPDATA/Sublime Text 3/Packages/Python" (convert-path ./Packages/Python)
```

Alternatively, download the portable version, and clone this repository directly as a subdirectory of the *Data* folder.

---

After you've finished, keep in mind that you're now overriding a default package. When Sublime Text updates to a new version, you'll run the risk of having an out-of-date package unless you pull the latest changes from this repository.

## Adding a new language

### Find an open-source `.tmLanguage` or `.sublime-syntax` file

- With a `.tmLanguage.json`, `.tmLanguage.yaml`, or other, convert to `.tmLanguage` first:
  - Install [the PackageDev plugin](https://github.com/SublimeText/PackageDev) in Sublime Text 3.
  - Open the file with Sublime Text 3, press <kbd>Cmd+Shift+P</kbd>.
  - Search for `PackageDev: Convert (YAML, JSON, PList) to` and select `Convert to: Property List`
  - Rename the file to just `.tmLanguage` instead of `.tmLanguage.plist` (Sublime will not recognize it as a tmLanguage file otherwise).
- With a `.tmLanguage` file:
  - example: https://github.com/Microsoft/TypeScript-TmLanguage/blob/master/TypeScript.tmLanguage
  - Ensure it has exact `.tmLanguage` suffix, or else command will not be available.
  - Open the file with Sublime Text 3, press <kbd>Cmd+Shift+P</kbd>.
  - Search for `Plugin Development: Convert Syntax to .sublime-syntax` command.

## Create a PR to this repository

Your PR should include:

- A folder like https://github.com/slimsag/Packages/tree/master/GraphQL with the final `.sublime-syntax` file.
- A `SOURCE` file with a URL where the syntax came from (e.g. link directly to the tmLanguage file on GitHub).
- A `VERSION` file with the Git commit hash of the SOURCE.
- An entry in the License table below, describing the license of the directory.

## License

All contents are licensed under the following licenses, which allow for free commercial use and distribution of the files:

All files are licensed under the [sublimehq/Packages](https://github.com/sublimehq/Packages) MIT + [Common License*](#common-license),
with different licenses for files generated by following the steps in a directory containing a SOURCE file:

| Directory                         | License               | Source                                                                                                                     |
|-----------------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| All, except those specified below | MIT + Common License* | [sublimehq/Packages](https://github.com/sublimehq/Packages)                                                                |
| VimL/                             | MIT                   | [evandroforks/VimL](https://github.com/evandroforks/VimL)                                                                  |
| Puppet/                           | MIT                   | [russCloak/SublimePuppet](https://github.com/russCloak/SublimePuppet)                                                      |
| Nix/                              | MIT                   | [rvantonder/sublime-nix](https://github.com/rvantonder/sublime-nix)                                                        |
| Move/                             | MIT                   | [rvantonder/move-sublime-highlighting](https://github.com/rvantonder/move-sublime-highlighting)                            |
| Julia/                            | MIT                   | [JuliaEditorSupport/Julia-sublime](https://github.com/JuliaEditorSupport/Julia-sublime)                                    |
| INI/                              | Apache-2.0            | [jwortmann/ini-syntax](https://github.com/jwortmann/ini-syntax)                                                            |
| Elm/                              | MIT                   | [elm-community/SublimeElmLanguageSupport](https://github.com/elm-community/SublimeElmLanguageSupport)                      |
| Coq/                              | MIT                   | [whitequark/Sublime-Coq](https://github.com/whitequark/Sublime-Coq)                                                        |
| Zig/                              | MIT                   | [ziglang/sublime-zig-language](https://github.com/ziglang/sublime-zig-language)                                            |
| TOML/                             | MIT                   | [sourcegraph/TOML-syntax-highlighting](https://github.com/sourcegraph/TOML-syntax-highlighting)                            |
| Terraform/                        | MIT                   | [alexlouden/Terraform.tmLanguage](https://github.com/alexlouden/Terraform.tmLanguage)                                      |
| GraphQL/                          | MIT                   | [rvantonder/gql-sublimetext-yolo](https://github.com/rvantonder/gql-sublimetext-yolo)                                      |
| DreamMaker/                       | MIT                   | [Wirewraith/sublime-DM](https://github.com/Wirewraith/sublime-DM)                                                          |
| Kotlin/                           | Apache License 2.0    | [vkostyukov/kotlin-sublime-package](https://github.com/vkostyukov/kotlin-sublime-package)                                  |
| Dockerfile/                       | Apache License 2.0    | [moby/moby](https://github.com/moby/moby/tree/master/contrib/syntax/textmate)                                              |
| COBOL/                            | Apache License 2.0    | [bitlang/sublime_cobol](https://bitbucket.org/bitlang/sublime_cobol)                                                       |
| Dart/                             | BSD 3-Clause License  | [guillermooo/dart-sublime-bundle-releases](http://github.com/guillermooo/dart-sublime-bundle-releases)                     |
| Cuda/                             | BSD 3-Clause License  | [harrism/sublimetext-cuda-cpp](https://github.com/harrism/sublimetext-cuda-cpp)                                            |
| Thrift/                           | Common License*       | [airamare01/thrift.tmbundle](https://github.com/airamare01/thrift.tmbundle)                                                |
| Smarty/                           | Common License*       | [amitsnyderman/sublime-smarty](https://github.com/amitsnyderman/sublime-smarty/blob/master/Syntaxes/Smarty.sublime-syntax) |
| Postscript/                       | Common License*       | [textmate/postscript.tmbundle](https://github.com/textmate/postscript.tmbundle)                                            |
| Plist/                            | Common License*       | [textmate/property-list.tmbundle](https://github.com/textmate/property-list.tmbundle)                                      |
| Ninja/                            | Common License*       | [textmate/ninja.tmbundle](https://github.com/textmate/ninja.tmbundle)                                                      |
| Mediawiki/                        | Common License*       | [slimsag/mediawiki.tmbundle](https://github.com/slimsag/mediawiki.tmbundle)                                                |
| Maven/                            | Common License*       | [textmate/maven.tmbundle](https://github.com/textmate/maven.tmbundle)                                                      |
| Man/                              | Common License*       | [textmate/man-pages.tmbundle](https://github.com/textmate/man-pages.tmbundle)                                              |
| Forth/                            | Common License*       | [textmate/forth.tmbundle](https://github.com/textmate/forth.tmbundle)                                                      |
| F#/                               | Common License*       | [textmate/f-sharp.tmbundle](https://github.com/textmate/f-sharp.tmbundle)                                                  |
| Cython/                           | Common License*       | [textmate/cython.tmbundle](https://github.com/textmate/cython.tmbundle)                                                    |
| Cron/                             | Common License*       | [textmate/cron.tmbundle](https://github.com/textmate/cron.tmbundle)                                                        |
| CapnProto/                        | Common License*       | [textmate/capnproto.tmbundle](https://github.com/textmate/capnproto.tmbundle)                                              |
| CMake/                            | Common License*       | [textmate/cmake.tmbundle](https://github.com/textmate/cmake.tmbundle)                                                      |
| ASP-VB-NET/                       | Common License*       | [textmate/asp.vb.net.tmbundle](https://github.com/textmate/asp.vb.net.tmbundle)                                            |
| Vue/                              | MIT License           | [vuejs/vue-syntax-highlight](https://github.com/vuejs/vue-syntax-highlight)                                                |
| TypeScript/                       | MIT License           | [rvantonder/TypeScript-Sublime-Plugin](https://github.com/rvantonder/TypeScript-Sublime-Plugin)                            |
| Swift/                            | MIT License           | [quiqueg/Swift-Sublime-Package](https://github.com/quiqueg/Swift-Sublime-Package)                                          |
| Stylus/                           | MIT License           | [billymoon/Stylus](https://github.com/billymoon/Stylus)                                                                    |
| Starlark/                         | MIT License           | [slimsag/vscode-bazel](https://github.com/slimsag/vscode-bazel/tree/patch-1/syntaxes)                                      |
| Smalltalk/                        | MIT License           | [textmate/smalltalk.tmbundle](https://github.com/textmate/smalltalk.tmbundle)                                              |
| SASS/                             | MIT License           | [slimsag/sass-textmate-bundle](https://github.com/slimsag/sass-textmate-bundle)                                            |
| Rust/                             | MIT License           | [rust-lang/rust-enhanced](https://github.com/rust-lang/rust-enhanced)                                                      |
| Protobuf/                         | MIT License           | [VcamX/protobuf-syntax-highlighting](https://github.com/VcamX/protobuf-syntax-highlighting)                                |
| PowerShell/                       | MIT License           | [slimsag/EditorSyntax](https://github.com/slimsag/EditorSyntax)                                                            |
| MSBuild/                          | MIT License           | [tillig/SublimeMSBuild](https://github.com/tillig/SublimeMSBuild)                                                          |
| LESS/                             | MIT License           | [textmate/less.tmbundle](https://github.com/textmate/less.tmbundle)                                                        |
| JavaScript/                       | MIT License           | [slimsag/Sublime-JS-Custom-Generated](https://github.com/slimsag/Sublime-JS-Custom-Generated/tree/master)                  |
| HLSL/                             | MIT License           | [MattSutherlin/HLSL_ST3](https://github.com/MattSutherlin/HLSL_ST3)                                                        |
| GLSL/                             | Unlicense             | [euler0/sublime-glsl](https://github.com/euler0/sublime-glsl)                                                              |
| Fish/                             | MIT License           | [Phidica/sublime-fish](https://github.com/Phidica/sublime-fish)                                                            |
| Ethereum/                         | MIT License           | [davidhq/SublimeEthereum](https://github.com/davidhq/SublimeEthereum)                                                      |
| Cg/                               | MIT License           | [noct/sublime-shaders](https://github.com/noct/sublime-shaders)                                                            |
| Elixir/                           | MIT License           | [princemaple/elixir-sublime-syntax](https://github.com/princemaple/elixir-sublime-syntax)                                  |
| Cue                               | MIT License           | [cue-sh/vscode-cue](https://github.com/cue-sh/vscode-cue)                                                                  |

### Common License*

This indicates a common license used in TextMate syntax/grammar bundles, which reads as follows:

> If not otherwise specified (see below), files in this repository fall under the following license:
>
>    Permission to copy, use, modify, sell and distribute this
>    software is granted. This software is provided "as is" without
>    express or implied warranty, and with no claim as to its
>    suitability for any purpose.
>
> An exception is made for files in readable text which contain their own license information, or files where an accompanying file exists (in the same directory) with a “-license” suffix added to the base-name name of the original file, and an extension of txt, html, or similar. For example “tidy” is accompanied by “tidy-license.txt”.

If an exception is made for the file we use, it must be noted as such in the table above.
