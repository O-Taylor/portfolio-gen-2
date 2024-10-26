<template>
  <div class="service-card">
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
    <router-link :to="contactLink" class="contact-link">Contact</router-link>
    <div class="block_icon">
      <div v-html="icon"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServiceCard',
  props: {
    title: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
    contactLink: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.service-card {
  border: 1px solid #ccc;
  padding: 16px;
  border-radius: 8px;
  text-align: left;
  width: 100%;
  background-color: #f9f9f9;
  transition: all 0.3s ease-in-out;
  color: #030f18;
  &:hover {
    color: #1477b5;
    background-color: #030f18;
    a {
      color: #fff;
    }
  }
  h2 {
    font-size: 1.5rem;
    margin: 0px;
    margin-bottom: 8px;
  }
  p {
    font-size: 1rem;
    margin: 0px;
    margin-bottom: 8px;
  }
  .contact-link {
    display: inline-block;
    margin-top: 8px;
    color: #030f18;
    text-decoration: none;
    transition: all 0.3s ease-in-out;
    &:hover {
      text-decoration: underline;
      color: #93a3b1;
    }
  }
  .block_icon {
    display: flex;
    justify-content: flex-end;
    margin-top: 8px;
  }
}
</style>
