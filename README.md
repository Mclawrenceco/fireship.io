## Fireship

The [Fireship PRO](https://fireship.io) course platform frontend is built with Svelte, Tailwind, Hugo, Firebase, and Flamethrower.

## Contributing

All static content is managed with Hugo in the `content` directory. You can easily fix typos by modifying the markdown directly on GitHub.

## How to Run

1. Install [Hugo Extended](https://gohugo.io/getting-started/installing/) version `0.101.0` or greater.
2. Clone the repository:
   ```sh
   git clone <this-repo>
   ```
3. Install dependencies:
   ```sh
   npm install
   ```
4. Start the development server:
   ```sh
   npm start
   ```
5. Open your browser and navigate to `http://localhost:6969/`.

## Developing Components

1. Create a Svelte file in the `app/components` directory with a custom element tag:
   ```svelte
   <svelte:options tag="hi-mom" />

   <script>
       export let greeting: string;
   </script>

   <h1>Hi Mom! {greeting}</h1>
   ```
2. Export the component from `app/main.ts`:
   ```ts
   export * from './components/hi-mom.svelte';
   ```
3. Use the component anywhere in your HTML or Markdown:
   ```html
   <hi-mom greeting="I made a web component"></hi-mom>
   ```

**Note:** Svelte web components require all styles to be encapsulated. You can use Tailwind, but only with `@apply` in the component. Global styles will not work.

## Commands

- `npm start`: Starts the main development server and runs everything you need.
- `npm run dev`: Runs components in isolation and serves `app/index.html` as a playground for components.
- `npm run hugo`: Only runs the static site.
- `npm run build`: Builds the project for production.
