<script>
  import {url} from '@sveltech/routify'
  export let id;
</script>

<h1>Article n°{id}</h1>

<a href={$url(`/blog/${id}/delete`)}>delete</a>