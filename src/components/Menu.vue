<template>
  <header class="header">
    <nav class="nav">
      <ul class="nav-links">
        <router-link to="/all" v-slot="{ href, navigate, isActive }">
          <li class="link">
              <a :href="href" :class="{'active-nav' : isActive}" @click="navigate">AllProducts</a>
          </li>
        </router-link>
        <router-link to="/smartphones" v-slot="{ href, navigate, isActive }">
          <li class="link">
            <a :href="href" :class="{'active-nav' : isActive}" @click="navigate">Smartphones</a>
          </li>
        </router-link>
        <router-link to="/notebooks" v-slot="{ href, navigate, isActive }">
          <li class="link">
            <a :href="href" @click="navigate" :class="{'active-nav' : isActive}">Notebooks</a>
          </li>
        </router-link>
      </ul>
    </nav>
    <slot></slot>
  </header>
</template>

<script>
export default {
};
</script>

<style>
  .header {
    width: 100%;
    height: 70px;
    background-color: #333333;
    box-sizing: border-box;
    padding: .5em;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .active-nav {
    color: #53AF61!important;
  }

  .nav {
    width: 600px;
  }

  .nav-links {
    width: 100%;
    display: flex;
    justify-content: flex-start;
  }

  .link {
    list-style: none;
    padding: 0 2em;
  }

  .link a {
    color: #fff;
    text-decoration: none;
  }

  a:active{
    color: #e74c3c;
  }
</style>
