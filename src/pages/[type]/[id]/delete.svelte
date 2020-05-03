<script>
  export let type;
  export let id;
  import {params, leftover} from '@sveltech/routify'
  type = $params.type;
</script>

<h1>Delete id {id} of type {type} ?</h1>