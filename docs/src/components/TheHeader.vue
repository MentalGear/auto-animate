<script setup lang="ts">
import TheLogo from "./TheLogo.vue"
import IconDiscord from "./IconDiscord.vue"
import IconTwitter from "./IconTwitter.vue"
import ColorModeToggle from "./ColorModeToggle.vue"
import GithubButton from "vue-github-button"
</script>

<template>
  <header>
    <TheLogo class="logo" />
    <div class="buttons">
      <a href="https://discord.gg/SHYT8pyeNm" aria-label="Discord"
        ><IconDiscord class="icon"
      /></a>
      <a href="https://twitter.com/useFormKit" aria-label="Twitter"
        ><IconTwitter class="icon"
      /></a>
      <GithubButton
        href="https://github.com/formkit/auto-animate"
        data-size="large"
        data-show-count="true"
        data-icon="star"
        aria-label="Star formkit/auto-animate on GitHub"
        >Star</GithubButton
      >
      <GithubButton
        href="https://github.com/sponsors/formkit"
        data-size="large"
        data-icon="heart"
        aria-label="Sponsor FormKit on GitHub"
        >Sponsor</GithubButton
      >
      <ColorModeToggle />
    </div>
  </header>
</template>

<style scoped>
header {
  height: 4em;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  padding-top: 2em;
  margin-bottom: 6em;
  justify-content: space-between;
  user-select: none;
}
.logo {
  width: 90%;
  max-width: 15em;
  margin-right: 1em;
  margin-bottom: 1em;
}

.buttons {
  display: flex;
  align-items: center;
}

.buttons a:hover {
  text-decoration: none;
}

.icon {
  width: 1.25em;
  fill: var(--gray-m);
  margin-right: 1em;
}
[data-dark-mode="true"] .icon {
  fill: var(--gray-l);
}

.buttons span {
  margin-right: 1em;
}
.buttons span:last-child {
  margin-right: 0;
}

.buttons a:hover .icon {
  fill: var(--primary);
}

@media (min-width: 700px) {
  header {
    padding-top: 1em;
    margin-bottom: 3em;
  }
  .logo {
    max-width: 12em;
    margin-bottom: 0;
  }
}
</style>
