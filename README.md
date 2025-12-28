# Portfolio Page
Following tutorial: https://www.youtube.com/watch?v=0YFrGy_mzjY (JS)
Following tutorial: https://www.youtube.com/watch?v=d56mG7DezGs (TS)

Tips (JS):
- Use Live Server on VSCode
    - Go to index.html
    - right click the text and click Open with Liver Server


What is TypeScript:
- Built on top of JavaScript
- Is a statically typed language (JS is not)

Steps (TS):
    - Install Node.js
    - run in terminal: npm i -g typescript
        - this installs TS in all folders
    - create a index.ts file

    Configuring TypeScript Compiler:
        - tsc --init 
            - creates tsconfig.json
        - create src and dist folders
        - in tsconfig.json
            - uncomment rootDir to go to ./src
            - uncomment outDir to go to ./dist
 
Tips for TS:
- running: tsc in terminal compiles all .ts files
- Debugging:
    - in tsconfig.json, have sourceMap to true
    - insert break points in code to start debugging
    - go to debug panel (in VSCode)
    - Click create a launch.json file
        - Select Node.js
    - in launch.json under "program"
        - add "preLaunchTask": "tsc: build - tsconfig.json",
            - tells compiler to use tsconfig.json
    - Now can debug!
        - go to debug panel, at top click "Launch Program"
        - In watch tab, you can add a variable to watch
        - step 