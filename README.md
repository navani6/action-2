# action-2
name: Generate ASCII artwork

on: 
    push
       branches:
           - main


jobs:
    ascii-art:
        runs-on:  ubuntu-latest

        steps:
            - name: checkout repository
              uses: actions/checkout@v4
            - name: execute shell script
              run: ./.github/workflows/ascii-script.sh