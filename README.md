# Yolol-Scripts
These are all scripts made by me. Hope they can be usefull out there.

Each file starts with the script, then has some information on why it should be used. And then more information on how to set it up!

If you have any questions Discord - Liperium#7591

name: Embed code in README

on:
  pull_request:
    branches:
      - main

jobs:
  embed-code:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
          persist-credentials: false # otherwise, the token used is the GITHUB_TOKEN, instead of your personal token
          fetch-depth: 0 # otherwise, you will failed to push refs to dest repo
          ref: refs/heads/${{ github.head_ref }}

      - uses: tokusumi/markdown-embed-code@main
        with:
          markdown: "README.md"
          token: ${{ secrets.GITHUB_TOKEN }}
          message: "synchronizing Readme"
          silent: true
