+++
title = "Install"
date = "2024-09-11T02:38:03-04:00"
author = "Adam McDaniel"
+++

# Install With Cargo

To install the `dunesh` binary on your machine with `cargo`, run the following command:

```sh
$ cargo install --git https://github.com/adam-mcdaniel/dune
```

# Post-Install

Dune doesn't function as a login shell, so it should mainly be used whenever you open a new terminal window or tab. If you want to use Dune in a script, you can call it directly with `dunesh`.

## Create A Dune Prelude

Dune uses a `.dune-prelude` file in the `$HOME` directory to setup the environment for your shell. This file is sourced by Dune every time it starts. You can use this file to set environment variables, define functions, or run any other shell commands you want to run every time you start a new shell session! 

> [The GitHub repository contains an example `.dune-prelude` file that calls a weather API to get the current climate in your area when it starts.](https://github.com/adam-mcdaniel/dune/blob/main/.dune-prelude)

It's also recommended to create a `.dune-secrets` file that your `.dune-prelude` can include. This file can contain your API keys and other secrets, while still allowing you to distribute your main config in the `.dune-prelude` file.

## Add To Shell Startup Script

Once you have `dunesh` on your system, add it to the non-login startup script for whatever shell your OS provides. For example, if you use `bash`, add the following line to your `~/.bashrc` file:

```sh
# At the end, start dune.
dunesh
```
