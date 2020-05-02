<script>
  export let type;
  export let id;
  import {params} from '@sveltech/routify'
  type = $params.type;
</script>

<h1>Delete id {id} of type {type} ?</h1>