<script setup>
import Card from './components/Card.vue';
const posts = [{
  tag:"React",
  title:'React 18 — Reactjs Latest Version to Bring Lots...',
  imgShow: true,
  data: "Chapter247",
  tagShow: true,
  horizontal: false,
  text: 'The extensively forecasted Version of React 18 has emerged finally. Its company has ultimately disclosed...',
  likes: '122',
  data_icon: true,
  ux: false,
  img_card: false,
  img_figma: false,



},{
  title:'How to Build a Design System if you’re...',
  imgShow: false,
  tagShow: false,
  data: "March 01, 2021",
  horizontal: false,
  text: 'It’s always hard to be the only person in a company who is responsible for product design. Your day can be insanely...',
  likes: '440',
  ux: false,
  img_card: false,
  img_figma: false,




},{
  tag:"React",
  title:'9 Figma design system tips',
  img_card: true,
  imgShow: false,
  data: "March 01, 2021",
  tagShow: true,
  horizontal: true,
  text: 'Most of these suggestions are ideal for when you’re dealing with design systems or huge design files, but they’re also...',
  likes: '111',
  ux: false,

},{
  tag:"Figma",
  title:'20 Figma plugins every designer must have',
  img_figma: true,
  imgShow: true,
  tagShow: true,
  vertical: true,
  horizontal: false,
  text: 'My favorite 20 plugins, which are important and necessary for every designer.',
  likes: '333',
  data: "Dinessamala",
  data_icon: false,
  ux: true,
  img_card: false,



} ]
</script>

<template>
  <div v-for="post in posts">
    
    <Card :img_card="post.img_card" :vertical="post.vertical" :ux="post.ux" :data_icon="post.data_icon" :likes="post.likes" :text="post.text" :key="post.key" :horizontal="post.horizontal" :tagShow="post.tagShow" :data="post.data" :title="post.title" :tag="post.tag" :img_figma="post.img_figma"/>
  </div>
</template>

<style scoped>
</style>
