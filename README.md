# Expense-Tracker
An Expense tracker app to be build using react.js [still under construction]

Front End application oriented to Expense tracking

## Technologies used

- [React](https://reactjs.org/) single page application
- Routing done using [React Router](https://reacttraining.com/react-router/web/guides/philosophy)
- State management via hooks(https://redux.js.org/) 

## Setup

1. Clone the repository and install the dependencies
```bash
npm install 
or
npm i
or
yarn install
```
2. Start the frontend application locally
```bash
npm start 
or
yarn start
```
3. add and track your expenses

## Available commands

* `yarn start`: Start the app locally in your development environment, by default it will be in http://localhost:3000.
* `yarn test`: Run tests using watch mode.
* `yarn lint`: Run linter.
* ... \[add other commands here\]

## Development flow

Here are the steps of the process you need to follow in order to integrate new code or a new feature into the project:

1. Transition the status of the card that describes the feature you will be working on in your issue tracker.
1. Create a local branch to get started using git: `git checkout -b <feature|bug|enhancement|doc>/<issue-tracker-number>-<short-description>`. For instance, this could be a branch name: `feature/96-add-navigation-sidebar`.
    * The first part indicates whether it is new feature, bug or documentation, while the second part it is just the issue tracker card number followed by some short description.
1. Develop the new feature while doing atomic commits to your local branch using `git commit`.
1. After you are done, you might want to do a `git rebase develop` in case new changes were integrated, so your new commits are applied on top of that and you make sure everything still works.
1. Before creating the Pull Request, you need to make sure the tests pass (`yarn test`).
1. Now you are ready to create a new Pull Request with your changes, but before, push your changes to origin using `git push -u origin <your-branch-name>`.
1. Your code should be reviewed, you can update the branch with new changes after you get some feedback.
1. After the Pull Request is approved, merge it using the UI on Github (you can also remove the branch directly from the same page, which is also convenient). Your code will land to the `develop` branch (and eventually deployed into the staging environment).
1. Finally, remember to transition your issue tracker card to `Done`.

### BEM convention

The components try to follow a [BEM](https://css-tricks.com/bem-101/) naming convention (Block Element Modifier). Hence, you can leverage the & (ampersand) operator in SASS to reference the parent component in a concise way.

```html
<a class="Button Button--big Button--orange">
  <span class="Button__price">$9.99</span>
  <span class="Button__text">Subscribe</span>
</a>
```

you can then write your styles as:

```CSS
.Button {
  &__price {
    text-align: right;
  }

  &__text {
    font-weight: bold;
  }

  &--big {
    font-size: 24px;
  }

  &--orange {
    color: darkorange;
  }
}
```
## Linter

In order to lint the code, the project uses [ESLint](https://eslint.org/), which is provided by [Create React App](https://github.com/facebook/create-react-app).

If you want to run the linter just type:
```bash
yarn lint
```

It's also convenient to integrate the linter warnings into your code editor, there are many plugins available for ESLint depending on your text editor used.


---

This app's css is completely written mannually 
