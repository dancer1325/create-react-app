# Code Splitting 

* [Code Splitting](/docusaurus/docs/code-splitting.md)

## How has it been created?

* `npx create-react-app code-splitting`

## How to run it?

* `npm run start`

## Notes
* `moduleA.js` + ALL its unique dependencies
  * separate chunk
  * | `onClick` event -> ONLY, then it's loaded