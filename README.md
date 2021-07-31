## Snippets

- `postcsstc` (postcss tailwind config)

```js
const tailwindcss = require("tailwindcss");

module.exports = {
	plugins: [
		tailwindcss("./tailwind.config.js"),
		require("autoprefixer"),
		process.env.NODE_ENV === "production"
			? require("@fullhuman/postcss-purgecss")({
					content: ["./src/**/*.js", "./public/index.html"],
					defaultExtractor: (content) =>
						content.match(/[A-Za-z0-9-_:/]+/g) || [],
			  })
			: "",
	],
};
```

- `mrfc` (material Ui react component)

```js
import React from "react";
import { makeStyles } from "@material-ui/core/styles";

const useStyles = makeStyles((theme) => ({}));
export default function () {
	const classes = useStyles();
	return <div></div>;
}
```

## dotenv for firebase and next.js

- `nfe` (next.js firebase env)

```
NEXT_PUBLIC_FIREBASE_API_KEY=""
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=""
NEXT_PUBLIC_FIREBASE_PROJECT_ID=""
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=""
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=""
NEXT_PUBLIC_FIREBASE_APP_ID=""
NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID=""
```
