<template>
  <header class="header">
    <nav class="navbar">
      <div class="container">
        <div class="inner">
          <div class="logo">
            <a href="/">otaylor.dev</a>
          </div>
          <div class="header_mobile_menu">
            <div class="hamburger" @click="toggleMobileMenu">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
          <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
      </div>
      <ul class="nav-links-mobile">
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'

// Define the toggleMobileMenu function here
const toggleMobileMenu = () => {
  const mobileMenu = document.querySelector('.nav-links-mobile')
  mobileMenu.classList.toggle('active')
}
</script>
<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" scoped>
.header {
  color: #bcb8b1;
  margin-top: 10px;
  position: sticky;
  top: 0;
  @media (max-width: 768px) {
    margin-top: 0px;
  }
  .navbar {
    position: relative;
    .container {
      max-width: 1350px;
      background-color: #030f18;
      margin: 0 auto;
      padding: 0px 25px;
      height: 100%;
      border-radius: 5px;
      overflow: hidden;
      @media (max-width: 768px) {
        padding: 0px 15px;
        border-radius: 0px;
      }
      .inner {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        position: relative;
        @media (max-width: 768px) {
          padding: 15px 0px;
        }
        .logo {
          a {
            color: #93a3b1;
            font-weight: 500;
            text-decoration: none;
            font-size: 1.5rem;
            transition: color 0.3s ease-in-out;
            &:hover {
              color: #2c394b;
            }
          }
        }
        .header_mobile_menu {
          display: none;
          @media (max-width: 768px) {
            display: block;
          }
          .hamburger {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 20px;
            width: 25px;
            cursor: pointer;
            span {
              height: 3px;
              width: 100%;
              background-color: #fff;
              border-radius: 5px;
            }
          }
        }
      }
      .nav-links {
        list-style: none;
        display: flex;
        gap: 10px;
        @media (max-width: 768px) {
          display: none;
        }
        a {
          color: #fff;
          text-decoration: none;
          transition: color 0.3s ease-in-out;
          &:hover {
            color: #93a3b1;
          }
        }
      }
    }
    .nav-links-mobile {
      display: none;
      @media (max-width: 768px) {
        display: flex;
        list-style: none;
        gap: 10px;
        margin: 0px;
        position: absolute;
        top: 100%;
        left: 0;
        background-color: #030f18;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 1000;
        height: 100vh;
        width: 100vw;
        padding: 0px;
        max-width: 0vw;
        overflow: hidden;
        transition: max-width 0.3s ease-in-out;
        &.active {
          max-width: 100vw;
        }
        a {
          color: #fff;
          text-decoration: none;
          transition: color 0.3s ease-in-out;
          &:hover {
            color: #93a3b1;
          }
        }
      }
    }
  }
}
</style>
