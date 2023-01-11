<script setup>
import { RouterLink, RouterView } from 'vue-router'
import VideoGames from './components/VideoGames.vue'
</script>

<template>
  <header>
    <div>
      <nav>
        <ul>
          <li><RouterLink to="/">VIDEO GAMES</RouterLink></li>
          <li><RouterLink to="/contact">CONTACT</RouterLink></li>
      </ul>
      </nav>
    </div>
  </header>

  <RouterView />
</template>



<style scoped>


.nav{
  position: sticky; /*(recomended)*/
  top: 0px;
  position: fixed; 
  margin: 20px;
}

 ul {
  list-style-type: none;
  margin: 10px;
  padding: 10px;
  overflow: hidden;
  position: sticky;
  top: 0;
}

 li {
  float: left;
  padding: 10px;
}

li.router-link-active,
li.router-link-exact-active
{
  text-shadow: 1px 1px 0px #ff0000;
}

 li a {
  display: block;
  text-align: center;
  padding: 30px;
  text-decoration: none;
  font-size: 30px;
}


</style>
