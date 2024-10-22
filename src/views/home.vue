<template>
  <TextImageHero :subTitle="tihSubTitle" :title="tihTitle" :text="tihText" />

  <TitleText :subTitle="sttSubTitle" :title="sttTitle" :text="sttText" />

  <!-- <ImageLeftTextRight
    :title="iltrTitle"
    :leftImage="leftImageBlockURL"
    :text="introText"
  /> -->
</template>

<script setup>
import ImageLeftTextRight from '@/components/content/image-left-text-right.vue'
import TextImageHero from '@/components/content/text-image-hero.vue'
import TitleText from '@/components/content/title-text.vue'
import profileImage from '@/assets/profile-shots/me.jpg'
const leftImageBlockURL = profileImage

// variable for ImageLeftTextRight component
const iltrTitle = 'Hi my names Oliver Taylor 👋'

const introText =
  'I am a full stack developer with a passion for creating beautiful and functional websites. I have experience with a range of technologies including HTML, CSS, JavaScript, Vue.js, Node.js, and MongoDB.'

// variables for TitleText component
const sttSubTitle = 'So whats the deal<i class="fa-solid fa-question"></i>'
const sttTitle = "You're probably wondering what I can do for you"
const sttText =
  'I can help you bring your ideas to life. I can help you create a website that is both beautiful and functional. I can help you create a website that is both beautiful and functional. I can help you create a website that is both beautiful and functional.'

// variable for TextImageHero component

const tihSubTitle = 'Your designs brought to life with code'
const tihTitle = 'Hi Welcome to my portfolio'
const tihText =
  'I focus on writing clean, elegant, and efficient code. I am always looking to improve my skills and learn new technologies. And always looking for new opportunities to work with a team of talented developers.'
</script>

<style scoped></style>
