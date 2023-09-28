<script lang="ts">
  import ProjectCard from "$lib/components/projectCard.svelte";

  import everPrev from "$lib/projects/everythingry.png";
  import steamLib from "$lib/projects/steamlibrarycompare.png";
</script>

<div class="flex flex-row justify-center">
  <div class="flex flex-col w-full gap-4">
    <div class="flex flex-row justify-center text-3xl">My Projects</div>
    <div class="grid grid-cols-4 mx-4">
      <ProjectCard
        title="Everythingry"
        image={everPrev}
        badges={["star", "Info", "Community Driven"]}
      >
        The concept behind this project was to act as my notebook. When I play a
        game, especially games that are especially info heavy like RPGS, I like
        having as much info at my disposal as possible. But doing so has become
        having 10 different wikis pulled up, so I've taken to the fundemental
        goal of adding new info whenever I have to look something up about a
        game.
      </ProjectCard>
      <ProjectCard
        title="Multi-Steam Library Compare"
        image={steamLib}
        badges={["star", "Tool"]}
      >
        This tool allows you to compare multiple Steam Libraries at the same
        time.
      </ProjectCard>
    </div>
  </div>
</div>
