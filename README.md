Reproduce the Bug

1. launch npm install
2. launch ./node_modules/.bin/eslint .

3. Get the error:



Oops! Something went wrong! :(

ESLint: 8.57.0

TypeError: Cannot read properties of undefined (reading 'members')
Occurred while linting sonar-fail/src/index.ts:2
Rule: "sonarjs/prefer-enum-initializers"
    at anyInitialized (sonar-fail/node_modules/eslint-plugin-sonarjs/lib/S6572/decorator.js:49:21)
    at sonar-fail/node_modules/eslint-plugin-sonarjs/lib/S6572/decorator.js:42:13
    at Object.report (sonar-fail/node_modules/eslint-plugin-sonarjs/lib/helpers/decorators/interceptor.js:71:29)
    at sonar-fail/node_modules/@typescript-eslint/eslint-plugin/dist/rules/prefer-enum-initializers.js:25:29
    at Array.forEach (<anonymous>)
    at TSEnumDeclaration (sonar-fail/node_modules/@typescript-eslint/eslint-plugin/dist/rules/prefer-enum-initializers.js:22:21)
    at ruleErrorHandler (sonar-fail/node_modules/eslint/lib/linter/linter.js:1076:28)
    at sonar-fail/node_modules/eslint/lib/linter/safe-emitter.js:45:58
    at Array.forEach (<anonymous>)
    at Object.emit (sonar-fail/node_modules/eslint/lib/linter/safe-emitter.js:45:38)

4. the source code only contains:

enum LogType {
  LOG,
  ERROR,
  WARN,
}
