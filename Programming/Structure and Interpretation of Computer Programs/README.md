# Structure and Interpretation of Computer Programs

## Scheme setup on macOS (10.15)

I installed MIT Scheme with Homebrew:

    $ brew install mit-scheme

Following [this Stack Overflow answer](https://stackoverflow.com/a/47724861), I added the following to my shell's startup run commands:

    runscheme () {
        scheme --quiet < "$1"
    }

This allows me to run scheme scripts without the interactive scheme shell:

    $ runscheme script.scm