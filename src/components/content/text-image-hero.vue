<template>
  <div class="text_image_hero">
    <div class="container">
      <div class="inner">
        <div class="text">
          <h3 v-html="props.subTitle"></h3>
          <h2 v-html="props.title"></h2>
          <p v-html="props.text"></p>
          <div class="buttons">
            <a href="javascript:" class="btn"> Get Started </a>
            <a href="javascript:" class="btn btn-secondary">Contact</a>
          </div>
        </div>
        <div class="left_image">
          <img :src="props.leftImage" alt="Placeholder Image" />
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
  subTitle: String,
  title: String,
  text: String,
})
</script>

<style lang="scss" scoped>
.text_image_hero {
  padding: 150px 0px;
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
        flex: 1;
        border-radius: 10px;
        img {
          height: 100%;
          width: 100%;
          object-fit: cover;
        }
      }
      .text {
        width: 70%;
        flex: 1;

        h3 {
          font-size: 0.9rem;
          margin: 0;
          padding-bottom: 10px;
          text-transform: uppercase;
          line-height: 1.5;
          color: #1477b5;
        }
        h2 {
          font-size: 4rem;
          text-transform: uppercase;
          margin: 0px;
          padding-bottom: 30px;
          line-height: 1;
          color: #030f18;
        }
        p {
          font-size: 1rem;
          line-height: 1.5;
          max-width: 75%;
          color: #030f18;
          margin: 0px;
          padding-bottom: 30px;
        }
        .buttons {
          display: flex;
          gap: 20px;

          .btn {
            display: block;
            background-color: #1477b5;
            color: #fff;
            padding: 10px 20px;
            text-transform: uppercase;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s ease-in-out;
            width: fit-content;
            &.btn-secondary {
              background-color: #030f18;
              &:hover {
                background-color: #1477b5;
              }
            }
            &:hover {
              background-color: #1a1a1a;
            }
          }
        }
      }
    }
  }
}
</style>
