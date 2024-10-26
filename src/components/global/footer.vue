<template>
  <footer class="site_footer">
    <nav class="navbar">
      <div class="container">
        <div class="inner">
          <div class="logo">
            <a href="/">otaylor.dev</a>
          </div>
          <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="sub_footer_nav">
      <p>otaylor.dev©</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss" scoped>
.site_footer {
  color: #bcb8b1;
  margin-top: 10px;
  position: sticky;
  top: 0;
  .navbar {
    min-height: 300px;
    background-color: #030f18;
    .container {
      max-width: 1350px;
      margin: 0 auto;
      padding: 0px 25px;
      height: 100%;
      border-radius: 5px 5px 0 0;
      overflow: hidden;
      .inner {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem;
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
      }
      .nav-links {
        list-style: none;
        display: flex;
        gap: 1rem;
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
  .sub_footer_nav {
    background-color: #fff;
    color: #030f18;
    text-align: center;
    padding: 5px;
    border-radius: 0 0 5px 5px;
  }
}
</style>
