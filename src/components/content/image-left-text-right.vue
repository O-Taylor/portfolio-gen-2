<template>
  <div class="image_left_text_right">
    <div class="container">
      <div class="inner">
        <div class="left_image">
          <img :src="props.leftImage" alt="Placeholder Image" />
        </div>
        <div class="text">
          <h2>{{ props.title }}</h2>
          <p>
            {{ props.text }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
// Define the "cards" prop here
const props = defineProps({
  leftImage: String,

  title: String,
  text: String,
})
</script>

<style lang="scss" scoped>
.image_left_text_right {
  padding: 50px 0px;
  .container {
    max-width: 1350px;
    margin: 0 auto;
    padding: 0px 25px;

    .inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 50px;
      max-width: 75%;
      margin: 0 auto;
      .left_image {
        height: 300px;
        width: 300px;
        img {
          height: 100%;
          width: 100%;
          object-fit: cover;
          border-radius: 10px;
        }
      }
      .text {
        width: 70%;
        h2 {
          font-size: 1.5rem;
          margin-bottom: 1rem;
        }
        p {
          font-size: 1rem;
          line-height: 1.5;
        }
      }
    }
  }
}
</style>
