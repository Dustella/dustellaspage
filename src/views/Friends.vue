<template>
  <header id="header">
    <nav>
      <ul v-for="i in links" :key="i.id">
        <li>
          <a :href="i.href" noreferrer="true">{{ i.name }}</a>
          <p>{{ i.description }}</p>
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
          name: "需要光的残影",
          href: "https://www.nya.al",
          description: "残影需要光",
        },
        {
          id: 2,
          name: "瓜瓜",
          href: "https://cd.al",
          description: "瓜瓜好帅啊",
        },
        {
          id: 3,
          name: "Julian",
          href: "https://jurt4201.blogspot.com/",
          description: "膜大佬Julian",
        },
        {
          id: 4,
          name: "超可爱的瑾知",
          href: "https://qingwu.top",
          description: "~超级可爱的瑾知~",
        },
      ],
    };
  },
});
</script>

<style scoped>
nav {
  display: flex;
  flex-direction: column;
}
li {
  width: 25vw;
  height: 15vh;
}
li > p {
  transform: translateY(0.5rem);
  font-size: 0.8rem;

}
@media screen and (max-width: 480px) {
  nav {
    flex-direction: column;
  }
}
</style>
