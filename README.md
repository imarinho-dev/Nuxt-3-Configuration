<h1 >Nuxt-3-Configuration</h1>

<h2 >Basic workflow configuration</h2>

<p>Create a new Nuxt 3 project by running the following command and following the prompts:</p>

```shell:
npx nuxi@latest init <project-name>
```

<p>Once the project is created, navigate into the project folder:</p>

```shell:
cd [project-name]
```

<p>Install the required dependencies with npm install</p>

```shell:
npm install
```

<p>Start the Nuxt development server:</p>

```shell:
npm run dev
```

<p>You can now access your Nuxt application by visiting <a href="http://localhost:3000" target="_blank">http://localhost:3000</a></p>

<h2>Nuxt Modules</h2>

<h3>TailwindCSS</h3>

<p>Install Tailwind CSS and its dependencies by running the following command:</p>

```shell:
npm install --save-dev @nuxtjs/tailwindcss
```

<p>Open the nuxt.config.js file in the root of your project directory and update the modules section to include the @nuxtjs/tailwindcss module:</p>

```javascript:
{
	modules: ['@nuxtjs/tailwindcss']
}
```

<p>Create a new file called tailwind.config.js in the root of your project directory and add the following code:</p>

```shell:
npx tailwindcss init
```

```javascript:
module.exports = {
	content: [
		'./components/**/*.{js,vue,ts}',
		'./layouts/**/*.vue',
		'./pages/**/*.vue',
		'./plugins/**/*.{js,ts}',
		'./nuxt.config.{js,ts}',
		'./app.vue'
	],
	theme: {
		extend: {}
	},
	plugins: []
};
```

Create a new tailwind.css file in your project's /assets/css/ and add the @tailwind directives for each of Tailwind’s layers.

```css:
@tailwind base;
@tailwind components;
@tailwind utilities;
```

<p>Create a new CSS file in your project's /assets/css folder. For example, you can create a file called main.css.</p>

<p>Add your global CSS styles to the main.css file. This can include styles for elements, classes, Google Fonts, or any other global styles you want to apply throughout your Nuxt application.</p>

```css:
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&display=swap');
```

<p>Open the nuxt.config.js file in the root of your project directory.</p>

<p>Inside the css array, add the path to your global.css file, relative to the root of your project. For example:</p>

```javascript:
css: ['@/assets/css/main.css'],
```

<h3>TailwindCSS automatic class sorting with Prettier</h3>

<p>Check out the plugin <a href="https://github.com/tailwindlabs/prettier-plugin-tailwindcss" target="_blank">on GitHub</a> learn more and get started.</p>

<p>To get started, install prettier-plugin-tailwindcss as a dev-dependency:</p>

```shell:
npm install -D prettier prettier-plugin-tailwindcss
```

<p>Then add the plugin to your Prettier config:</p>

```javascript:
// prettier.config.js
module.exports = {
  plugins: ['prettier-plugin-tailwindcss'],
}
```
