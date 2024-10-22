<template>
  <div class="title_text">
    <div class="container">
      <div class="inner">
        <div class="text">
          <h3 v-html="props.subTitle"></h3>
          <h2 v-html="props.title"></h2>
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
  subTitle: String,
  title: String,
  text: String,
})
</script>

<style lang="scss" scoped>
.title_text {
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
        h3 {
          font-size: 0.9rem;
          margin: 0;
          text-align: center;
          text-transform: uppercase;
          line-height: 1.5;
          color: #1477b5;
          padding-bottom: 20px;
        }
        h2 {
          font-size: 2rem;
          text-transform: uppercase;
          text-align: center;
          margin: 0px;
          padding-bottom: 20px;
          line-height: 1;
          color: #030f18;
        }
        p {
          font-size: 1rem;
          line-height: 1.5;
          text-align: center;
          max-width: 50%;
          color: #030f18;
          margin: auto;
          padding-bottom: 30px;
        }
      }
    }
  }
}
</style>
