<script lang="ts">
  import "../app.css";
  let theme: string = "dark";

  function swapTheme() {
    if (theme == "dark") {
      theme = "light";
    } else {
      theme = "dark";
    }
  }
</script>

<div data-theme={theme}>
  <div class="flex flex-col h-screen gap-4">
    <div class="flex flex-row h-2/5 justify-center items-center relative">
      <div class="absolute w-full h-full banner blur-sm z-0" />
      <div class="z-10 text-6xl font-bold text-yellow-400">Void Baroness</div>
    </div>
    <div class="flex-1">
      <slot />
    </div>
    <footer class="footer p-10 bg-base-300 text-base-content">
      <nav>
        <header class="footer-title">Socials</header>
        <a class="link link-hover" href="https://twitter.com/VoidBaroness">Twitter</a>
        <a class="link link-hover" href="https://www.youtube.com/@VoidBaroness">YouTube</a>
        <a class="link link-hover" href="https://www.twitch.tv/voidlinghub">Twitch</a>
      </nav>
    </footer>
  </div>

  <div class="flex flex-row absolute top-4 w-full justify-center">
    <div class="w-4/5">
      <div class="navbar bg-base-300 rounded-full">
        <div class="navbar-start">
          <div class="dropdown">
            <!-- svelte-ignore a11y-label-has-associated-control -->
            <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
            <label tabindex="0" class="btn btn-ghost btn-circle">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                ><path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h7"
                /></svg
              >
            </label>
            <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
            <ul
              tabindex="0"
              class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
            >
              <li><a href="/projects">Projects</a></li>
              <li><a href="/socials">Socials</a></li>
            </ul>
          </div>
        </div>
        <div class="navbar-center">
          <!-- svelte-ignore a11y-missing-attribute -->
          <a class="btn btn-ghost normal-case text-xl" href="/"
            >The Voidling Hub</a
          >
        </div>
        <div class="navbar-end pr-4">
          <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
          <label class="swap swap-rotate" on:mousedown={swapTheme}>
            <input type="checkbox" />
            <div class="swap-off">
              <svg
                class="fill-current w-6 h-6"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                ><path
                  d="M21.64,13a1,1,0,0,0-1.05-.14,8.05,8.05,0,0,1-3.37.73A8.15,8.15,0,0,1,9.08,5.49a8.59,8.59,0,0,1,.25-2A1,1,0,0,0,8,2.36,10.14,10.14,0,1,0,22,14.05,1,1,0,0,0,21.64,13Zm-9.5,6.69A8.14,8.14,0,0,1,7.08,5.22v.27A10.15,10.15,0,0,0,17.22,15.63a9.79,9.79,0,0,0,2.1-.22A8.11,8.11,0,0,1,12.14,19.73Z"
                /></svg
              >
            </div>
            <div class="swap-on">
              <svg
                class="fill-current w-6 h-6"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                ><path
                  d="M5.64,17l-.71.71a1,1,0,0,0,0,1.41,1,1,0,0,0,1.41,0l.71-.71A1,1,0,0,0,5.64,17ZM5,12a1,1,0,0,0-1-1H3a1,1,0,0,0,0,2H4A1,1,0,0,0,5,12Zm7-7a1,1,0,0,0,1-1V3a1,1,0,0,0-2,0V4A1,1,0,0,0,12,5ZM5.64,7.05a1,1,0,0,0,.7.29,1,1,0,0,0,.71-.29,1,1,0,0,0,0-1.41l-.71-.71A1,1,0,0,0,4.93,6.34Zm12,.29a1,1,0,0,0,.7-.29l.71-.71a1,1,0,1,0-1.41-1.41L17,5.64a1,1,0,0,0,0,1.41A1,1,0,0,0,17.66,7.34ZM21,11H20a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Zm-9,8a1,1,0,0,0-1,1v1a1,1,0,0,0,2,0V20A1,1,0,0,0,12,19ZM18.36,17A1,1,0,0,0,17,18.36l.71.71a1,1,0,0,0,1.41,0,1,1,0,0,0,0-1.41ZM12,6.5A5.5,5.5,0,1,0,17.5,12,5.51,5.51,0,0,0,12,6.5Zm0,9A3.5,3.5,0,1,1,15.5,12,3.5,3.5,0,0,1,12,15.5Z"
                /></svg
              >
            </div>
          </label>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .banner {
    background-repeat: no-repeat;
    background-position-y: 40%;
    background-size: cover;
    background-image: url($lib/banner.png);
  }
</style>
