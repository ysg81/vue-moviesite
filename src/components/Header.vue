<template>
  <header>
    <Logo />
    <div class="nav nav-pills">
      <div 
        v-for="nav in navigations"
        :key="nav.name"
        class="nav-item">

        <RouterLink 
          :to="nav.href"
          active-class="active"
          class="nav-link">
          {{ nav.name }}
        </RouterLink>

      </div>
    </div>
  </header>
</template>

<script>
import Logo from './Logo'
export default {
  components: {
    Logo
  },
  data(){
    return {
      navigations: [
        {
          name: 'Search',
          href: '/'
        },
        {
          name: 'Movie',
          href: '/movie'
        },
        {
          name: 'About',
          href: '/about'
        }
      ]
    }
  }
}
</script>


<style scoped>
  header {
    height: 70px;
    padding: 0 40px;
    display: flex;
    align-items: center;
  }
  header .logo{
    margin-right: 40px;
  }
</style>