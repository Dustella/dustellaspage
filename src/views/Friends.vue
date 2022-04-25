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

<script lang="ts" setup>
const links = [
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
  },{
    id: 3,
    name:"lixiang810",
    href: "https://stblog.penclub.club/",
    description: "膜lixiang810"
  },
  {
    id: 4,
    name: "Julian",
    href: "https://jurt4201.blogspot.com/",
    description: "啥都玩的Julian",
  },
  {
    id: 5,
    name: "超可爱的瑾知",
    href: "https://qingwu.top",
    description: "~超级可爱的瑾知~",
  },
];
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
