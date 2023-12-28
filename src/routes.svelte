<script lang="ts">
  import Router, { link } from "svelte-spa-router";
  import Home from "./routes/Home.svelte";
  import Dummy from "./routes/Dummy.svelte";
  import NotFound from "./routes/NotFound.svelte";

  if (window.location.pathname !== "/") {
    window.location.replace("/#" + window.location.pathname);
  }

  const routes = {
    "/": Home,
    "/url": Dummy,
    "*": NotFound,
  };
</script>

<Router {routes} />
