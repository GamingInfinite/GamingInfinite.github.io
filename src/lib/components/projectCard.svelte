<script lang="ts">
  export let title;
  export let badges;
  export let image;
</script>

<div class="card w-96 bg-base-100 shadow-xl">
  <figure><img src={image} alt={title} /></figure>
  <div class="card-body">
    <h2 class="card-title">
      {title}
      {#if badges.includes("star")}
        <div class="badge badge-outline">Premier</div>
      {/if}
    </h2>
    <p class="line-clamp-3">
      <slot />
    </p>
    <div class="card-actions justify-end">
      {#each badges as badge}
        {#if !(badge == "star")}
          <div class="badge badge-outline">{badge}</div>
        {/if}
      {/each}
    </div>
  </div>
</div>
