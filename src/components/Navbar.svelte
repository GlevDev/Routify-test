<script>
  import { url, isActive } from "@sveltech/routify";
  const links = [
    { path: "/index", name: "Home" },
    { path: "/about", name: "About" },
    { path: "/articles", name: "Articles" }
  ];
</script>

<style>
  .navlink {
    display: flex;
    align-items: center;
    justify-content: left;
    margin: 1rem;
  }

  .active {
    background: rgba(0,0,0,0.3);
  }

  .navlink div {
    margin-right: 1rem;
  }

  .navlink div a {
    padding: 5px;
  }
</style>

<div class="navlink">
  {#each links as link}
    <div>
      <a href={$url(link.path)} class:active={$isActive(link.path)}>{link.name}</a>
    </div>
  {/each}
</div>
