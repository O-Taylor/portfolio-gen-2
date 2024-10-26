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
        <div class="right_image" v-if="rightImage">
          <img
            :src="props.rightImage"
            alt="Hero image positioned on the right"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
// Define the "cards" prop here
const props = defineProps({
  rightImage: String,
  subTitle: String,
  title: String,
  text: String,
})
</script>

<style lang="scss" scoped>
.text_image_hero {
  padding: 150px 0px;
  @media (max-width: 768px) {
    padding: 50px 0px;
  }
  .container {
    max-width: 1350px;
    margin: 0 auto;
    padding: 0px 25px;
    @media (max-width: 768px) {
      padding: 0px 15px;
    }

    .inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 50px;
      @media (max-width: 768px) {
        flex-direction: column;
      }

      .right_image {
        height: 500px;
        width: 50%;
        flex: 1;
        border-radius: 10px;
        overflow: hidden;
        @media (max-width: 768px) {
          width: 100%;
          height: 300px;
        }
        img {
          height: 100%;
          width: 100%;
          object-fit: cover;
        }
      }
      .text {
        width: 70%;
        flex: 1;
        @media (max-width: 768px) {
          width: 100%;
        }

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
          @media (max-width: 768px) {
            font-size: 2.2rem;
          }
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
