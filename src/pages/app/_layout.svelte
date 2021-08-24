<!-- routify:options preload="proximity" -->
<script>
  import TopNavbar from "../../_components/topNavbar.svelte";
  import Navbar from "../../_components/navbar.svelte";
</script>

<div class="bg-base-100 text-base-content min-h-screen" data-theme="forest">
  <header>
    <TopNavbar />
  </header>
  <main class="py-28 bg-base-100 text-base-content">
    <div class="container mx-auto px-6 lg:mx-0 bg-base-100 text-base-content">
      <slot />
    </div>
  </main>
  <footer><Navbar /></footer>
</div>
