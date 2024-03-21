<script>
  import Stack from './lib/Stack.svelte'
  const frontends = ["Svelte", "React", "Vue", "jQuery","Angular", "Preact", "Solid", "Lit", "Alpine.js", "HTML/JS", "Astro", "Marco"]
  const bundlers = ["Vite", "Webpack", "Rollup", "Parcel", "Parcel 2", "Gulp", "Grunt"]
  const styles = ["Sass", "PostCSS", "Vanilla", "Tailwind", "MUI", "jQuery UI", "Bootstrap", "Materialize", "Bulma", "Foundation", "Semantic UI", "UIKit"]
  const backends = ["Node", "Express", "Fastify", "Koa", "Hapi", "WordPress", "Drupal", "Umbraco", "Laravel", "Django", "Ruby on Rails", "REST", "GraphQL", "Flat file", "PHP"]
  const deployments = ["Old-school FTP", "GitHub Pages", "Netlify", "Vercel", "Cloudflare Pages", "Render", "Heroku", "Now", "AWS", "GCP", "Azure", "Fly.io"]
  
  
  const metas = ["SvelteKit", "Sapper", "Nuxt", "Next.js", "Gatsby"]
  const tools = ["TypeScript", "ESLint", "Prettier"]
</script>

<main>
  <h1>Tech-Stack-Generator</h1>
  <p class="bold">How about a:</p>
  <div class="row">
    <Stack items={frontends}/> frontend
  </div>
  <div class="row">
    with <Stack items={bundlers}/> under the hood
  </div>
  <div class="row">
  styled with <Stack items={styles}/>
  </div>
  <div class="row">
  using a <Stack items={backends}/> backend
  </div>
  <div class="row">
    deployed on <Stack items={deployments}/>
  </div>
</main>


