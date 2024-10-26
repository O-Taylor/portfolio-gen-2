<template>
  <div class="services_block">
    <div class="container">
      <div class="inner">
        <div class="services_grid">
          <service-card
            v-for="card in cards"
            :key="card.id"
            :title="card.title"
            :text="card.text"
            :icon="card.icon"
            :contactLink="card.contactLink"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ServiceCard from '@/components/cards/service-card.vue'
import { defineProps } from 'vue'
// Define the "cards" prop here

const props = defineProps({
  leftImage: String,

  title: String,
  text: String,
})

const cards = [
  {
    id: 1,
    title: 'Mobile First',
    text: 'I build websites that work on all devices. Desktop, tablet, or mobile: your site will be responsive!',
    icon: '<i class="fa-solid fa-mobile"></i>',
    contactLink: '/contact',
  },
  {
    id: 2,
    title: 'SEO Friendly',
    text: 'I follow best practices to ensure your site ranks well on search engines.',
    icon: '<i class="fa-solid fa-magnifying-glass"></i>',
    contactLink: '/contact',
  },
  {
    id: 3,
    title: 'Fast Load Times',
    text: 'My websites are optimized for speed. I use the latest techniques to make your site load fast!',
    icon: '<i class="fa-solid fa-bolt-lightning"></i>',
    contactLink: '/contact',
  },
  {
    id: 4,
    title: 'Latest Technologies',
    text: 'I use the latest technologies to build your site, so it looks and feels modern and fresh.',
    icon: '<i class="fa-solid fa-code"></i>',
    contactLink: '/contact',
  },
  {
    id: 5,
    title: 'Best Practices',
    text: 'I follow best practices to ensure your site is secure and easy to maintain.',
    icon: '<i class="fa-solid fa-book"></i>',
    contactLink: '/contact',
  },
  {
    id: 6,
    title: 'Collaborative by Nature',
    text: 'I work closely with my clients to ensure their vision is brought to life.',
    icon: '<i class="fa-solid fa-hand-holding-heart"></i>',
    contactLink: '/contact',
  },
]
</script>

<style lang="scss" scoped>
.services_block {
  padding: 40px 0px;
  .container {
    max-width: 1350px;
    margin: 0 auto;
    padding: 0px 25px;
    @media (max-width: 768px) {
      padding: 0px 15px;
    }
    .inner {
      .services_grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 15px;
        @media (max-width: 900px) {
          grid-template-columns: repeat(2, 1fr);
        }
        @media (max-width: 768px) {
          grid-template-columns: 1fr;
        }
      }
    }
  }
}
</style>
