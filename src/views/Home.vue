<template>
  <header id="header">
    <div class="content">
      <div class="inner">
        <h1>{{ mainpage.title }}</h1>
        <p>{{ mainpage.subTitle }}</p>
      </div>
    </div>

    <nav>
      <ul v-for="i in links" :key="i.id">
        <li>
          <a :href="i.href">{{ i.name }}</a>
        </li>
      </ul>
    </nav>
  </header>
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
      mainpage: {
        title: "Dustella Here",
        subTitle: "啦啦啦啦",
        copyright: "Dustella",
      },
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
