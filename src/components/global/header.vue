<template>
  <header class="header">
    <nav class="navbar">
      <div class="container">
        <div class="inner">
          <div class="logo">
            <a href="/">My Portfolio</a>
          </div>
          <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

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
  .container {
    max-width: 1350px;
    background-color: #030f18;
    margin: 0 auto;
    padding: 0px 25px;
    height: 100%;
    border-radius: 5px;
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
</style>
