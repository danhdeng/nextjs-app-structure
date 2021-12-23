# Steps to setup the project

yarn create next-app project-name

touch tsconfig.json

yarn dev

yarn add --dev typescript @types/react @types/node

yarn add eslint -

# eslint configuration

yarn eslint --init

$ E:\Code\nextjs\nextjs-app-structure\node_modules\.bin\eslint --init
√ How would you like to use ESLint? · style
√ What type of modules does your project use? · esm
√ Which framework does your project use? · react
√ Does your project use TypeScript? · No / Yes
√ Where does your code run? · browser
√ How would you like to define a style for your project? · guide
√ Which style guide do you want to follow? · google
√ What format do you want your config file to be in? · JavaScript
Checking peerDependencies of eslint-config-google@latest
The config that you've selected requires the following dependencies:

eslint-plugin-react@latest @typescript-eslint/eslint-plugin@latest eslint-config-google@latest eslint@>=5.16.0 @typescript-eslint/parser@latest
√ Would you like to install them now with npm? · No / Yes
Installing eslint-plugin-react@latest, @typescript-eslint/eslint-plugin@latest, eslint-config-google@latest, eslint@>=5.16.0, @typescript-eslint/parser@latest

# update the eslintrc.js to avoid the bug that eslint can not detect the latest version of React

settings: {
react: {
version: 'latest',
},
},

# add prettier to project

yarn add prettier -D

# add estlint-config-prettier to avoid prettier conflcit with eslint

yarn add eslint-config-prettier -D

# add prettier to the estlintrc.js file in the extends attribute

extends: ['plugin:react/recommended', 'google', 'prettier'],

# add prettier config file

touch .prettierrc.js

# format the whole code with prettier under current directory

yarn prettier --write .

# create .vscode folder to store settings.json file for settings on the specific project.

.vscode/settings.json

{
"editor.formatOnPaste": true,
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.codeActionsOnSave": {
"source.fixAll.eslint": true,
"source.fixAll.format": true
}
}

#
