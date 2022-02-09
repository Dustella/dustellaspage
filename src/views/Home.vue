<template>
  <nav>
    <ul v-for="i in links" :key="i.id">
      <li>
        <a :href="i.href">{{ i.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  data() {
    return {
      links: [
        {
          id: 1,
          name: "博客",
          href: "https://blog.dustella.net",
        },
        {
          id: 2,
          name: "朋友们",
          href: "/friends",
        },
        {
          id: 3,
          name: "杂货铺",
          href: "https://index.dustella.net",
        },
      ],
    };
  },
});
</script>

<style scoped>
nav {
  display: flex;
  flex-direction: row;
}
@media screen and (max-width: 480px) {
  nav {
    flex-direction: column;
  }
}
</style>