# Unity TestResults Parser

This is a tool to parse Unity test results, designed for use in CI/CD
environments.

## Building

Following the standard `stack` procedures should be enough to get you going.

    $ stack setup
    $ stack build
    $ stack exec unity-testresult-parser -- [args] [files]

## CLI Options

The parser supports a number of CLI options.

1. `-h,--help`: show the help menu
2. `-c,--color=yes|no|auto`: colorize the output
    * things that pass (100% passing) are colorized green
    * things that fail (at least one fail) are colorized red
    * if we somehow don't know the result, it is colorized orange
3. `-q,--quiet`: only show non-passing results
4. `-s,--summary`: print a (maybe) colorized result at the end of the output
   that counts passes and failures
