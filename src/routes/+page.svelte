<script>
  import Greet from "$lib/Greet.svelte";
  import { checkUpdate } from "@tauri-apps/api/updater";

  async function checkForUpdates() {
    const update = await checkUpdate();
    console.log(update);
  }
</script>

<h1>Welcome to Tauri!</h1>

<div class="row">
  <a href="https://vitejs.dev" target="_blank" rel="noreferrer">
    <img src="/vite.svg" class="logo vite" alt="Vite Logo" />
  </a>
  <a href="https://tauri.app" target="_blank" rel="noreferrer">
    <img src="/tauri.svg" class="logo tauri" alt="Tauri Logo" />
  </a>
  <a href="https://kit.svelte.dev" target="_blank" rel="noreferrer">
    <img src="/svelte.svg" class="logo svelte" alt="Svelte Logo" />
  </a>
</div>

<p>Click on the Tauri, Vite, and Svelte logos to learn more.</p>
<button style="margin: 30px;" on:click={checkForUpdates}
  >Check for Updates</button
>

<div class="row">
  <Greet />
</div>

<style>
  .logo.vite:hover {
    filter: drop-shadow(0 0 2em #747bff);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00);
  }
</style>
