# Structure and Interpretation of Computer Programs

I am using the second edition of the book, which can be read for free [as a website](https://mitpress.mit.edu/sites/default/files/sicp/full-text/book/book.html) and as a [pdf](http://web.mit.edu/alexmv/6.037/sicp.pdf). I will be following only the book, and not the related lecture series recommended by [teachyourselfcs.com](https://teachyourselfcs.com/#programming).

## Scheme setup on macOS (10.15)

I installed MIT Scheme with Homebrew:

    $ brew install mit-scheme

Following [this Stack Overflow answer](https://stackoverflow.com/a/47724861), I added the following to my shell's startup run commands:

    runscheme () {
        scheme --quiet < "$1"
    }

This allows me to run scheme scripts without the interactive scheme shell:

    $ runscheme script.scm