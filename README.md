## Snippets

- `postcsstc` (postcss tailwind config)

```js
const tailwindcss = require('tailwindcss');

module.exports = {
	plugins: [
		tailwindcss('./tailwind.config.js'),
		require('autoprefixer'),
		process.env.NODE_ENV === 'production'
			? require('@fullhuman/postcss-purgecss')({
					content: ['./src/**/*.js', './public/index.html'],
					defaultExtractor: (content) =>
						content.match(/[A-Za-z0-9-_:/]+/g) || [],
			  })
			: '',
	],
};
```

- `mrfc` (material Ui react component)

```js
import React from 'react';
import { makeStyles } from '@material-ui/core/styles';

const useStyles = makeStyles((theme) => ({}));
export default function () {
	const classes = useStyles();
	return <div></div>;
}
```
