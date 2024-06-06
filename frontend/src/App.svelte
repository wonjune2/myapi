<script>
  import Router from 'svelte-spa-router';
  import Detail from "./routes/Detail.svelte";
  import Home from "./routes/Home.svelte";

  const routes = {
    '/': Home,
    '/detail/:question_id': Detail,
  }
</script>

<Router {routes}/>
