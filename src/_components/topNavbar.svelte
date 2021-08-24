<script>
  import Logo from "./logo.svelte";
  import Icon from "./icon.svelte";
  import Sidebar from "./sidebar.svelte";
</script>

<div
  class="flex justify-between items-center w-full fixed py-4 px-4 glass z-10 top-0 left-0 right-0"
>
  <Sidebar />
  <div class="space-x-3">
    <button class=" btn-sm md:btn-md btn btn-ghost"
      ><span><Icon name="search" /></span></button
    >
    <button class="btn-sm md:btn-md btn btn-ghost"
      ><span style="transform: rotate(90deg);"
        ><Icon name="dots-horizontal" /></span
      ></button
    >
  </div>
</div>
