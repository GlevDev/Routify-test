<script>
  import { url, isActive } from "@sveltech/routify";
  const links = [
    { path: "/index", name: "Home" },
    { path: "/about", name: "About" },
    { path: "/articles", name: "Articles" }
  ];
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap');

  .navlink {
    display: flex;
    align-items: center;
    justify-content: left;
    background: #f6f6f6;
  }

  .active {
    border-bottom: 2px solid red !important;
  }

  .navlink div {
    margin-right: 1rem;
  }

  .navlink div a {
    padding: 10px;
    text-decoration: none;
    font-size: 1.2rem;
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    color: #333;
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
