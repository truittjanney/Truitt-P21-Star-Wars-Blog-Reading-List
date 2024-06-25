Introduction:
- The Star Wars Blog Reading List is an online blog for Star Wars lore. It includes information about Star Wars characters, planets, and vehicles.

Features:
- Add favorites

Technologies Used:
- Bootstrap
- JavaScript
- React
- SWAPI.tech API

Requirements:
- Make sure you are using node version 10

1. Install the packages:
```
$ npm install
```
2. Create a .env file:
```
$ cp .env.example .env
```
3. Start coding! and the webpack dev server with live reload, for Windows, Mac, Linux or Gitpod:

```bash
$ npm run start
```

Styles:
- You can update the `styles/index.css` or create new `.css` files inside `styles/` and import them into your current scss or js files depending on your needs.

Components:
- Add more files into your `./src/js/components` or styles folder as you need them and import them into your current files as needed.

**Note (New changes)**: Components have been converted into functions to support the use of hooks:
- Instead of a class component, we're using a `const` function.
- Class `constructor` and `state` have been replaced by `useState()` hooks.
- `componentDidMount()` was replaced by `useEffect({}, [])` - It runs at mount thanks to the second parameter (`[]`).
- `Actions` and `Store` still work the same way.

```jsx
// Previous "Class Oriented"
export class Demo extends React.Component {
	constructor(props) {
		super(props);

		this.state = getState('code here');
	}
}

// New "Functional Oriented"
export const Demo = () => (
	const [state, setState] = getState('code here'); //using the state (if needed)
  const { store, actions } = useContext(Context); // using the context (if needed)

);
```

Note: There is an example using the Context API inside `views/demo.js`;

Views (Components):
- Add more files into your `./src/js/views` and import them in `./src/js/layout.jsx`.

Context:
- This boilerplate comes with a centralized general Context API. The file `./src/js/store/flux.js` has a base structure for the store, we encourage you to change it and adapt it to your needs.

- React Context [docs](https://reactjs.org/docs/context.html)

- The `Provider` is already set. You can consume from any component using the useContext hook to get the `store` and `actions` from the Context. Check `/views/demo.js` to see a demo.

```jsx
import { Context } from "../store/appContext";
const MyComponentSuper = () => {
  //here you use useContext to get store and actions
  const { store, actions } = useContext(Context);
  return <div>{/* you can use your actions or store inside the html */}</div>
}
```

How to use the Star Wars Blog Reading List:
- Click on the lore that you are interested in reading whether that is characters, planets, or vehicles. You can favorite any of the readings you like the most by clicking the star icon.

Contributors:
- Truitt Janney (https://github.com/truittjanney)

We welcome contributions from the community! How to contribute:
- Search existing issues before creating a new issue. Please check to see if it has already been reported. This helps us avoid duplicates.
- If you cannot find an existing issue, you can create a new one. Please provide detailed information about the problem, including steps to reproduce, expected behavior, and any relevant screenshots.

Making Changes:
- 1) Fork the repository - Start by forking the repository to your GitHub account.
- 2) Clone the repository - Clone your forked repository to your local machine using 'git clone https://github.com/your-username/your-repo-name.git
- 3) Create a new branch - Create a new branch for your changes. Use a descriptive name for your branch to identify the feature or fix you are working on.
- 4) Use the command 'git checkout -b your-branch-name'
- 5) Make your changes - Make your changes to the codebase. Ensure your code follows the project's coding standards and passes all tests.

Committing & Pushing Changes:
- 1) Commit your changes - Once you have made and tested your changes, commit them with a clear and concise commit message. Then push your changes to your forked repository.
- 2) Use the command 'git add .'
- 3) Use the command 'git commit -m "Description of the changes"'
- 4) Use the command 'git push origin your-branch-name'

Creating a Pull Request:
- 1) Navigate to the original repository - Go to the original repository where you want to submit your changes.
- 2) Create a pull request - Click on the "New Pull Request" button. Ensure your branch is compared with the correct branch in the original repository (usually "main" or "master").
- 3) Describe your changes - Provide a detailed description of your changes in the pull request. Mention any related issues and explain why the changes are necessary.
- 4) Submit the pull request - Submit your pull request and wait for the maintainers to review it.

Code Review & Feedback:
- Respond to feedback - The maintainers may request changes to your pull request. Be sure to respond to feedback promptly and make the necessary updates.
- Merge approval - Once your pull request is approved, it will be merged into the main codebase.

Best Practices for Contributing:
- Write clear commit messages - Make sure your commit messages are clear and descriptive.
- Follow coding standards - Adhere to the coding standards and guidelines specified in the repository.
- Test your changes - Ensure that your changes do not break existing functionality and pass all tests.
- Document your changes - Update any relevant documentation to reflect your changes.

Thank you for your interest in contributing to our project!
