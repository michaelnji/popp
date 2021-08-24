<script>
  import { isActive, url } from "@roxi/routify";
  import { fly } from "svelte/transition";

  import Icon from "./icon.svelte";
  import Logo from "./logo.svelte";
  // js code for sidebar
  let sidebarIsActive = false;
  const activateHandler = () => {
    sidebarIsActive = !sidebarIsActive;
  };
  console.log($isActive("/app/Overview"));
</script>

<button class="btn btn-ghost" on:click={activateHandler}>
  <Icon name="grid-view" />
</button>
{#if sidebarIsActive}
  <div
    class="sidebar absolute min-h-screen z-50  bg-base-100 text-base-content  top-0 left-0 rounded-tr-box rounded-br-box shadow-lg flex flex-col items-start justify-start py-4 lg:w-4/12 w-11/12 sm:w-6/12 "
    transition:fly
  >
    <header class="w-full flex justify-between items-center pr-2 ">
      <Logo />
      <button
        class="btn btn-ghost hover:bg-primary hover:bg-opacity-20 hover:text-primary"
        on:click={activateHandler}><Icon name="x" /></button
      >
    </header>
    <div class="w-full border-b opacity-20" />

    <div class="mt-6 pb-2 pr-4 overflow-hidden">
      <a href="/app/Overview">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Overview")}
        >
          <Icon name="home" config="mr-8" /><b class="ml-8">Overview</b>
        </div>
      </a>
      <a href="/app/Agenda">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Agenda")}
        >
          <Icon name="flag" config="mr-8" /><b class="ml-8">Agenda</b>
        </div>
      </a>
      <a href="/app/Calendar">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Calendar")}
        >
          <Icon name="calendar" config="mr-8" /><b class="ml-8">Calendar</b>
        </div>
      </a>
      <a href="/app/Goals">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Goals")}
        >
          <Icon name="star" config="mr-8" /><b class="ml-8">Goals</b>
        </div>
      </a>
      <a href="/app/Grades">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Grades")}
        >
          <Icon name="hashtag" config="mr-8" /><b class="ml-8">Grades</b>
        </div>
      </a>
      <a href="/app/Timetable">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Timetable")}
        >
          <Icon name="archive" config="mr-8" /><b class="ml-8">Timetable</b>
        </div>
      </a>
      <a href="/app/Subjects">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Subjects")}
        >
          <Icon name="clip" config="mr-8" /><b class="ml-8">Subjects</b>
        </div>
      </a>
    </div>
    <div class="w-full border-b opacity-20" />
    <div class="mt-auto pr-4 overflow-hidden">
      <a href="/app/FAQ">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/FAQ")}
        >
          <Icon name="heart" config="mr-8" /><b class="ml-8">FAQ</b>
        </div>
      </a>
      <a href="/app/Settings">
        <div
          class="w-full flex pl-6 pr-28  py-4 my-1 rounded-tr-full rounded-br-full hover:bg-primary hover:bg-opacity-10 hover:text-primary transition-all duration-300 ease-out"
          class:active={$isActive("/app/Settings")}
        >
          <Icon name="cog" config="mr-8" /><b class="ml-8">Settings</b>
        </div>
      </a>
    </div>
  </div>
{/if}

<style>
  /* styles for sidebar */
  .active {
    @apply bg-opacity-10 bg-primary text-primary mr-4 rounded-br-full rounded-tr-full;
  }
</style>
