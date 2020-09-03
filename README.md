# DevCrev Base Project: TypeScript, VS Code, ESLint

## How this project was made:

I am using VS Code with the ESLint (by Dirk Baeumer) extension installed.

I already have Node.js/NPM installed on my Linux machine.

I do not have TypeScript installed globally but I will install it locally to the project.

I do not have ESLint installed globally but I will install it locally to the project.

## Let's get started.

Start from a directory where you want create the project folder.

Make a project directory.

`$ mkdir typescript-eslint-hello`

Change into that directory.

`$ cd typescript-eslint-hello/`

Initialize the project.

`$ npm init -y`

Install TypeScript.

`$ npm install --save-dev typescript`

Install ESLint.

`$ npm install --save-dev eslint`

Configure ESLint.

`$ ./node_modules/.bin/eslint --init`

- Questions and answers while configuring ESLint:
    - How would you like to use ESLint?
        - To check syntax and find problems
    - What type of modules does your project use?
        - CommonJS
    - Which framework does your project use?
        - None of these
    - Does your project use TypeScript?
        - Yes
    - Where does your code run?
        - Browser
    - What format do you want your config file to be in?
        - JSON
    - Would you like to install them now with npm?
        - Yes

Launch VS Code.

`$ code .`

Edit package.json and replace the scripts section with what is committed in this repository.

Add app.ts and populate it with what is in the repository.

Edit .eslintrc.json
- Change the env > "es2021" key to "es2020". The value remains true.
- Change the parserOptions > "ecmaVersion" value from 12 to 11.
- I suspect the above two changes will not be needed after a future update of the VS Code ESlint extension.
- Replace the empty rules section with what is committed in this repository.

Save all files.

For app.ts (opened in editor) you should see red error indicators for missing semicolons and a yellow warning indicator for the use of the console method.

![ShowErrors](./ShowErrors.png?raw=true "Showing Errors")

For the npm scripts:
- `$ npm run lint`
    - Will lint all .ts files
- `$ npm run build`
    - Will build app.js from app.ts
