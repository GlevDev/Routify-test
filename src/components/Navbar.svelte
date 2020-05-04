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
    background: #dddddd;
  }

  .active {
    border-bottom: 2px solid red !important;
  }

  .navlink div {
    margin-right: 1rem;
  }

  .navlink div a {
    text-decoration: none;
    display: block;
    height: 100%;
    border-bottom: 2px solid transparent;
    float: left;
  }
</style>

<div class="navlink">
  {#each links as link}
    <div>
      <a href={$url(link.path)} class:active={$isActive(link.path)}>{link.name}</a>
    </div>
  {/each}
</div>
