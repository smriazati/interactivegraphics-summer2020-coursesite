<template>
 <header>

  <div v-if="pageType == 'Home'">
    <div class="site-title">
      <h1>Home</h1>
    </div>
    <nav>
      <h2>Courses:</h2>
      <ul>
        <li><nuxt-link to="/interactive-graphics-01/">Interactive Graphics Summer 2020</nuxt-link></li>
      </ul>
    </nav>     
  </div>

  <div v-if="pageType == 'Course'">
    <div class="site-title">
      <h1>Interactive Graphics Summer 2020</h1>
    </div>
    <nav>
      <ul>
        <li><nuxt-link to="/interactive-graphics-01/syllabus">Syllabus</nuxt-link></li>
        <li><nuxt-link to="/interactive-graphics-01/labs">Labs</nuxt-link></li>
        <li><nuxt-link to="/interactive-graphics-01/resources">Resources</nuxt-link></li>
        <li><nuxt-link to="/interactive-graphics-01/gallery">Gallery</nuxt-link></li>
      </ul>
    </nav>     
  </div>

 </header>

</template>


<script>
export default {

  data() {
    return {
      
    }
  },
  computed: {
    pageType() {
      if(this.$route.path === '/') {
        return 'Home';
      } else {
        return 'Course';
      }
    }
  }


}
</script>
<style lang="scss" scoped>

$dark: #000;
$light: #fff;
$purple: #667aff;

h1 {
  color: $purple;
  font-size: 3rem;
}

</style>
