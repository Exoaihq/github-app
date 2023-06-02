# Exo AI Github App Documentation

## Installation

Navigate to the app home page and install to your account or individual repository

## How it works

https://www.youtube.com/watch?v=kZzDE2Tyc1M

1. A webhook is sent to the Exo server when a PR is opened
2. The server checks the changes in the PR's commits and creates a prompt for the LLM: 

```
const prompt = `Please write a test for the follow git output changes:
    ${patch}
    If the changes are not testable, for example a console log or an imported function or an actual test function, please return null with no other explanation.
  `;
```
3. If a valid test is created a commit is pushed to the PR's branch with the code in a `.test` file
4. You can then pull down the changes locally and run/update/remove the test

## Uninstall

In Github click on Settings --> Applications --> Configuration --> Uninstall "Exoaihq"




