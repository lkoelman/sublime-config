This is my personal Sublime Text configuration.

# Useful Extensions

Not all of these are installed.

## General extensions

- SublimeLinter
- Markdown Extended
- Monokai Extended
- [Emacs Pro Essentials](https://packagecontrol.io/packages/Emacs%20Pro%20Essentials)
- [AceJump](https://github.com/ice9js/ace-jump-sublime)

## Git integration

- GitSavvy
- GitGutter

## Python extensions

- PythonImproved
- SublimeLinter
- SublimeLinter-Pyflakes
    + = program / syntax errors only
- SublimeLinter-Flake8
    + = pep8 + pyflakes

```
pip install pyflakes flake8
```

SublimeLinter.sublime-settings:

```json
{
    "debug": false, // Set to true to print extra information in the console.
    "linters": {
        // Flake8 = PEP8 style guide + pyflakes program errors
        // example config: https://packagecontrol.io/packages/Python%20Flake8%20Lint
        "flake8": {
            "executable": "/home/luye/anaconda2/bin/flake8",
            "disable": true,        // pyflakes should be enough
            // What to lint
            "ignore": "",           // ignored error codes
            "pyflakes": true,       // turn on pyflakes error lint
            "pep8": false,          // turn on pep8 error lint
            "pydocstyle": false,    // turn on pydocstyle error lint
            "naming": false,        // turn on naming error lint
            "debugger": true,       // turn on debugger error lint
            // Look & Feel
            "gutter_marks": "theme-simple"
        },
        // Pyflakes = program & syntax errors only
        "pyflakes": {
            "executable": "/home/luye/anaconda2/bin/pyflakes",
            "disable": false,
            "ignore": "",           // ignored error codes
            "gutter_marks": "theme-simple"
        }
    }
    
}
```

## Lisp extensions

`Parinfer`

## Rust extensions

- `RustEnhanced` -> official Rust plugin

- `LSP` -> optional dependency of RustEnhanced
    - completion, goto definition, find references
    - install dependencies using `rustup`

- [RACER](https://github.com/racer-rust/racer)
    - for autocompletion of libraries/functions
    - see github page for most up-to-date Sublime plugin

## C++ extensions

- https://packagecontrol.io/packages/EasyClangComplete
- https://packagecontrol.io/packages/Clang%20Format

Syntax Definition:

- C Improved
- C++ Starting Kit
- C++ 11

Linting:

- https://packagecontrol.io/packages/SublimeLinter-cppcheck
- https://packagecontrol.io/packages/SublimeLinter-clang

Misc:

- https://packagecontrol.io/packages/SublimeGDB
- https://packagecontrol.io/packages/CMake
- https://packagecontrol.io/packages/CTags
