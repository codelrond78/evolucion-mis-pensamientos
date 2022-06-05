<!-- _post.svelte -->
<script>
    import Gitter from '../../lib/components/_gitter.md'    
    export let title
    export let date
  </script>
  
  <article class="prose lg:prose-xl">
    <h1>{title}</h1>
  
    <p>Published: {date}</p>
    
    <Gitter />

    <slot />

  </article>
  